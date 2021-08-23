---
title: Benutzererstellung mit dem ADSI LDAP-Anbieter
description: Mit dem ADSI LDAP-Anbieter können Sie nur ein globales Benutzerkonto erstellen.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- LDAP-Anbieter ADSI, Benutzerobjekt, Benutzererstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023068"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Benutzererstellung mit dem ADSI LDAP-Anbieter

Mit dem ADSI LDAP-Anbieter können Sie nur ein globales Benutzerkonto erstellen. Lokale Konten befinden sich in der SAM-Datenbank und müssen mit dem WinNT-Anbieter erstellt werden. Weitere Informationen zum Erstellen eines Benutzerobjekts mit dem WinNT-Anbieter finden Sie unter [WinNT-Benutzerobjekt.](winnt-user-object.md)

**So erstellen Sie ein Benutzerobjekt**

1.  Binden Sie an den Container, in dem sich das Benutzerobjekt befindet, und rufen Sie entweder die [**IADsContainer-**](/windows/desktop/api/Iads/nn-iads-iadscontainer) oder [**die IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) für den Container ab.
2.  Verwenden Sie die [**IADsContainer.Create-**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) oder [**IDirectoryObject::CreateDSObject-Methode,**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) um das Benutzerobjekt zu erstellen.
3.  Welche Attribute zum Erstellen eines Benutzerobjekts mindestens erforderlich sind, hängt vom verwendeten Verzeichnisdienst ab. Weitere Informationen zum Erstellen eines Active Directory-Benutzers finden Sie unter [Erstellen eines Benutzers.](/windows/desktop/AD/creating-a-user)
4.  Wenn die [**IADsContainer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet wird, wird das neue Objekt erst erstellt, wenn die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufgerufen wird.

    Wenn die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verwendet wird, wird das neue Objekt erstellt, wenn die [**CreateDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) aufgerufen wird. Die minimalen Attribute, einschließlich [**objectClass,**](/windows/desktop/ADSchema/a-objectclass)müssen im [**ADS \_ ATTR \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) angegeben werden, das an die **CreateDSObject-Methode** übergeben wird.

## <a name="example-1"></a>Beispiel 1

Im folgenden Codebeispiel wird ein Benutzerkonto mit den Standardattributen erstellt.


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



## <a name="example-2"></a>Beispiel 2

Im folgenden Codebeispiel wird ein Benutzerkonto mit den Standardattributen erstellt. Aus Gründen der Kürze wird die Fehlerüberprüfung ausgelassen.


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



 

 