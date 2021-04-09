---
title: Benutzer Erstellung mit dem ADSI-LDAP-Anbieter
description: Mit dem ADSI LDAP-Anbieter können Sie nur ein globales Benutzerkonto erstellen.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- LDAP-Anbieter ADSI, Benutzerobjekt, Benutzer Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104050824"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="53a4c-104">Benutzer Erstellung mit dem ADSI-LDAP-Anbieter</span><span class="sxs-lookup"><span data-stu-id="53a4c-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="53a4c-105">Mit dem ADSI LDAP-Anbieter können Sie nur ein globales Benutzerkonto erstellen.</span><span class="sxs-lookup"><span data-stu-id="53a4c-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="53a4c-106">Lokale Konten befinden sich in der SAM-Datenbank und müssen mit dem WinNT-Anbieter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="53a4c-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="53a4c-107">Weitere Informationen zum Erstellen eines Benutzer Objekts mit dem WinNT-Anbieter finden Sie unter [Winnt-Benutzerobjekt](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="53a4c-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="53a4c-108">**So erstellen Sie ein Benutzerobjekt**</span><span class="sxs-lookup"><span data-stu-id="53a4c-108">**To create a user object**</span></span>

1.  <span data-ttu-id="53a4c-109">Binden Sie an den Container, in dem sich das Benutzerobjekt befindet, und rufen Sie entweder die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -oder die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle für den Container ab.</span><span class="sxs-lookup"><span data-stu-id="53a4c-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="53a4c-110">Verwenden Sie die [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) -Methode oder die [**IDirectoryObject:: roatedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) -Methode, um das Benutzerobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="53a4c-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="53a4c-111">Die minimalen Attribute, die zum Erstellen eines Benutzer Objekts erforderlich sind, hängen vom verwendeten Verzeichnisdienst ab.</span><span class="sxs-lookup"><span data-stu-id="53a4c-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="53a4c-112">Weitere Informationen zum Erstellen eines Active Directory Benutzers finden Sie unter [Erstellen eines Benutzers](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="53a4c-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="53a4c-113">Wenn die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle verwendet wird, wird das neue-Objekt erst erstellt, wenn die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="53a4c-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="53a4c-114">Wenn die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle verwendet wird, wird das neue-Objekt erstellt, wenn die Methode " [**samatedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="53a4c-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="53a4c-115">Die minimalen Attribute (einschließlich der [**objectClass**](/windows/desktop/ADSchema/a-objectclass)) müssen im [**ADS- \_ \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) Array angegeben werden, das an die Methode " **kreatedsobject** " übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="53a4c-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="53a4c-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53a4c-116">Example 1</span></span>

<span data-ttu-id="53a4c-117">Im folgenden Codebeispiel wird ein Benutzerkonto mit den Standard Attributen erstellt.</span><span class="sxs-lookup"><span data-stu-id="53a4c-117">The following code example creates a user account with the default attributes.</span></span>


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="53a4c-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53a4c-118">Example 2</span></span>

<span data-ttu-id="53a4c-119">Im folgenden Codebeispiel wird ein Benutzerkonto mit den Standard Attributen erstellt.</span><span class="sxs-lookup"><span data-stu-id="53a4c-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="53a4c-120">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="53a4c-120">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 