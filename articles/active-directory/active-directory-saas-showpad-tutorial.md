---
title: "チュートリアル: Azure Active Directory と Showpad の統合 | Microsoft Docs"
description: "Azure Active Directory と Showpad の間でシングル サインオンを構成する方法について説明します。"
services: active-directory
documentationcenter: 
author: jeevansd
manager: femila
editor: 
ms.assetid: 48b6bee0-dbc5-4863-964d-75b25e517741
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 02/15/2017
ms.author: jeedes
translationtype: Human Translation
ms.sourcegitcommit: b2eb87a88721a3fd1ecdfa573c6a6d49ed02d344
ms.openlocfilehash: 6912357da797a72f8e9cb9ebf700f56d9cfcc696
ms.lasthandoff: 02/16/2017


---
# <a name="tutorial-azure-active-directory-integration-with-showpad"></a>チュートリアル: Azure Active Directory と Showpad の統合
このチュートリアルの目的は、Showpad と Azure Active Directory (Azure AD) を統合する方法を説明することです。

Showpad と Azure AD の統合には、次の利点があります。

* Showpad にアクセスする Azure AD ユーザーを制御できます。
* ユーザーが自分の Azure AD アカウントで自動的に Showpad にサインオン (シングル サインオン) できるようにします。
* 1 つの中央サイト (Azure Active Directory ポータル) でアカウントを管理できます。

SaaS アプリと Azure AD の統合の詳細については、「 [Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](active-directory-appssoaccess-whatis.md)」を参照してください。

## <a name="prerequisites"></a>前提条件
Showpad と Azure AD の統合を構成するには、次のものが必要です。

* Azure AD サブスクリプション
* Showpad サブスクリプション

> [!NOTE]
> このチュートリアルの手順をテストする場合、運用環境を使用しないことをお勧めします。
> 
> 

このチュートリアルの手順をテストするには、次の推奨事項に従ってください。

* 必要な場合を除き、運用環境は使用しないでください。
* Azure AD の評価環境がない場合は、 [こちら](https://azure.microsoft.com/pricing/free-trial/)から&1; か月の評価版を入手できます。

## <a name="scenario-description"></a>シナリオの説明
このチュートリアルの目的は、テスト環境で Azure AD のシングル サインオンをテストできるようにすることです。 

このチュートリアルで説明するシナリオは、主に次の&2; つの要素で構成されています。

1. ギャラリーからの Showpad の追加
2. Azure AD シングル サインオンの構成とテスト

## <a name="adding-showpad-from-the-gallery"></a>ギャラリーからの Showpad の追加
Azure AD への Showpad の統合を構成するには、ギャラリーから管理対象 SaaS アプリの一覧に Showpad を追加する必要があります。

**ギャラリーから Showpad を追加するには、次の手順を実行します。**

1. **Azure クラシック ポータル**の左側のナビゲーション ウィンドウで、**[Active Directory]** をクリックします。 
   
    ![アプリケーション][1]

2. **[ディレクトリ]** の一覧から、ディレクトリ統合を有効にするディレクトリを選択します。

3. アプリケーション ビューを開くには、ディレクトリ ビューでトップ メニューの **[アプリケーション]** をクリックします。
   
    ![[アプリケーション]][2]

4. ページの下部にある **[追加]** をクリックします。
   
    ![アプリケーション][3]

5. **[実行する内容]** ダイアログで、**[ギャラリーからアプリケーションを追加します]** をクリックします。
   
    ![アプリケーション][4]

6. 検索ボックスに、「 **Showpad**」と入力します。
   
    ![アプリケーション](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_01.png)

7. 結果ウィンドウで **[Showpad]** を選択し、**[完了]** をクリックしてアプリケーションを追加します。
   
    ![アプリケーション](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_02.png)

## <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成とテスト
このセクションの目的は、"Britta Simon" というテスト ユーザーに基づいて、Showpad で Azure AD のシングル サインオンを構成し、テストする方法について説明することです。

シングル サインオンを機能させるには、Azure AD ユーザーに対応する Showpad ユーザーが Azure AD で認識されている必要があります。 言い換えると、Azure AD ユーザーと Showpad の関連ユーザーの間で、リンク関係が確立されている必要があります。

このリンク関係を確立するには、Azure AD の **[ユーザー名]** の値を Showpad の **[Username]** の値として割り当てます。

Showpad で Azure AD のシングル サインオンを構成してテストするには、次の構成要素を完了する必要があります。

1. **[Azure AD シングル サインオンの構成](#configuring-azure-ad-single-single-sign-on)** - ユーザーがこの機能を使用できるようにします。
2. **[Azure AD のテスト ユーザーの作成](#creating-an-azure-ad-test-user)** - Britta Simon で Azure AD のシングル サインオンをテストします。
3. **[Showpad テスト ユーザーの作成](#creating-a-showpad-test-user)** - Showpad で Britta Simon に対応するユーザーを作成し、Azure AD の Britta Simon にリンクさせます。
4. **[Azure AD テスト ユーザーの割り当て](#assigning-the-azure-ad-test-user)** - Britta Simon が Azure AD のシングル サインオンを使用できるようにします。
5. **[シングル サインオンのテスト](#testing-single-sign-on)** - 構成が機能するかどうかを確認します。

### <a name="configuring-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成
このセクションの目的は、Azure クラシック ポータルで Azure AD のシングル サインオンを有効にすることと、Showpad アプリケーションでシングル サインオンを構成することです。

**Showpad で Azure AD シングル サインオンを構成するには、次の手順を実行します。**

1. Azure クラシック ポータルの **Showpad** アプリケーション統合ページで **[シングル サインオンの構成]** をクリックし、**[シングル サインオンの構成]** ダイアログを開きます。
   
    ![Configure Single Sign-On][6] 

2. **[ユーザーの Showpad へのアクセスを設定してください]** ページで、**[Microsoft Azure AD シングル サインオン]** を選択し、**[次へ]** をクリックします。
   
    ![Configure Single Sign-On](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_03.png)

3. **[アプリケーション設定の構成]** ダイアログ ページで、次の手順を実行し、**[次へ]** をクリックします。
   
    ![[シングル サインオンの構成]](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_04.png) 

    a. **[サインオン URL]** ボックスに、次のパターンを使用して、ユーザーが Showpad アプリケーションへのサインオンに使用する URL を入力します。`https://<company name>.showpad.biz/login`

    b. **[識別子]** ボックスに、`https://<company name>.showpad.biz` のパターンを使用して URL を入力します。

    c. **[次へ]**


1. **[Showpad シングル サインオン パラメーターの構成]** ページで、次の手順を実行し、**[次へ]** をクリックします。
   
    ![[シングル サインオンの構成]](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_05.png)
   
    a.[サインオン URL] ボックスに、次のパターンを使用して、ユーザーが Yardi eLearning アプリケーションへのサインオンに使用する URL を入力します。 **[メタデータのダウンロード]** をクリックし、コンピューターにファイルを保存します。
   
    b. **[次へ]**をクリックします。

2. Showpad テナントに管理者としてサインオンします。

3. 上部のメニューで **[Settings]**をクリックします。
   
    ![アプリ側でのシングル サインオンの構成](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_001.png) 

4. **[Single Sign-On]** に移動して **[Enable]** をクリックします。
   
    ![アプリ側でのシングル サインオンの構成](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_002.png)

5. **[Add a SAML 2.0 Service ]** ダイアログで、次の手順を実行します。
   
    ![アプリ側でのシングル サインオンの構成](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_003.png) 
   
    a. **[Name (名前)]** ボックスに、ID プロバイダーの名前 (会社名など) を入力します。
   
    b. **[Metadata Source]** として、**[XML]** を選択します。
   
    c. ダウンロードしたメタデータ XML ファイルの内容をコピーし、**[Metadata XML]** ボックスに貼り付けます。
   
    d. **[Auto-provision accounts for new users when they log in]** を選択します。
   
    e. **[送信]**をクリックします。

6. Azure クラシック ポータルで、シングル サインオンの構成確認を選択し、 **[次へ]**をクリックします。
   
    ![Azure AD のシングル サインオン][10]

7. **[シングル サインオンの確認]** ページで、**[完了]** をクリックします。  
   
    ![Azure AD のシングル サインオン][11]

### <a name="creating-an-azure-ad-test-user"></a>Azure AD のテスト ユーザーの作成
このセクションの目的は、Azure クラシック ポータルで Britta Simon というテスト ユーザーを作成することです。

![Azure AD ユーザーの作成][20]

**Azure AD で Showpad テスト ユーザーを作成するには、次の手順を実行します。**

1. **Azure クラシック ポータル**の左側のナビゲーション ウィンドウで、**[Active Directory]** をクリックします。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_09.png) 

2. **[ディレクトリ]** の一覧から、ディレクトリ統合を有効にするディレクトリを選択します。

3. 上部のメニューで **[ユーザー]**をクリックして、ユーザーの一覧を表示します。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_03.png) 

4. 下部にあるツール バーで **[ユーザーの追加]** をクリックして、**[ユーザーの追加]** ダイアログ ボックスを開きます。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_04.png) 

5. **[このユーザーに関する情報の入力]** ダイアログ ページで、次の手順に従います。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_05.png) 
   
    a. **[ユーザー名]** ボックスに「**BrittaSimon**」と入力します。
   
    b. **[次へ]**をクリックします。

6. **[ユーザー プロファイル]** ダイアログ ページで、次の手順に従います。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_06.png) 
   
    a.[サインオン URL] ボックスに、ユーザーが Tidemark アプリケーションへのサインオンに使用する URL を入力します。 **[名]** ボックスに「**Britta**」と入力します。  
   
    b. **[姓]** ボックスに「**Simon**」と入力します。
   
    c. **[表示名]** ボックスに「**Britta Simon**」と入力します。
   
    d. **[ロール]** として **[ユーザー]** を選びます。
   
    e. **[次へ]**をクリックします。

7. **[一時パスワードの取得]** ダイアログ ページで、**[作成]** をクリックします。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_07.png)

8. **[一時パスワードの取得]** ダイアログ ページで、次の手順に従います。
   
    ![Azure AD のテスト ユーザーの作成](./media/active-directory-saas-showpad-tutorial/create_aaduser_08.png) 
   
    a.[サインオン URL] ボックスに、次のパターンを使用して、ユーザーが Yardi eLearning アプリケーションへのサインオンに使用する URL を入力します。 **[新しいパスワード]** の値を書き留めます。
   
    b. ページの下部にある **[完了]**」を参照してください。

### <a name="creating-a-showpad-test-user"></a>Showpad テスト ユーザーの作成
このセクションの目的は、Showpad で Britta Simon というユーザーを作成することです。 

Showpad では、ジャストインタイム プロビジョニングがサポートされています。 プロビジョニングは、「 **[Azure AD シングル サインオンの構成](#configuring-azure-ad-single-single-sign-on)**」を参照してください。 

このセクションでは必要な操作はありません。 

### <a name="assigning-the-azure-ad-test-user"></a>Azure AD テスト ユーザーの割り当て
このセクションの目的は、Britta Simon に Showpad へのアクセスを許可することで、このユーザーが Azure のシングル サインオンを使用できるようにすることです。

![ユーザーの割り当て][200]

**Showpad に Britta Simon を割り当てるには、次の手順を実行します。**

1. Azure クラシック ポータルの上部にあるメニューで、 **[アプリケーション]**をクリックします。
   
    ![ユーザーの割り当て][201] 
2. アプリケーションの一覧で **[Showpad]**をクリックします。
   
    ![[シングル サインオンの構成]](./media/active-directory-saas-showpad-tutorial/tutorial_showpad_50.png) 
3. 上部のメニューで **[ユーザー]**をクリックします。
   
    ![ユーザーの割り当て][203]
4. ユーザーの一覧で **[Britta Simon]**を選択します。
5. 下部にあるツール バーで **[割り当て]**をクリックします。
   
    ![ユーザーの割り当て][205]

### <a name="testing-single-sign-on"></a>シングル サインオンのテスト
このセクションの目的は、アクセス パネルを使用して Azure AD のシングル サインオン構成をテストすることです。

アクセス パネルで **[Showpad]** タイルをクリックすると、自動的に Showpad アプリケーションにサインオンします。

## <a name="additional-resources"></a>その他のリソース
* [SaaS アプリと Azure Active Directory を統合する方法に関するチュートリアルの一覧](active-directory-saas-tutorial-list.md)
* [Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](active-directory-appssoaccess-whatis.md)

<!--Image references-->

[1]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_04.png

[6]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_05.png
[10]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_06.png
[11]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_07.png
[20]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-showpad-tutorial/tutorial_general_205.png

