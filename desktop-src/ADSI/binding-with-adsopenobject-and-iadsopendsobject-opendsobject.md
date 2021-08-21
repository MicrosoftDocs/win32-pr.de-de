---
title: Binden mit ADsOpenObject und IADsOpenDSObject OpenDSObject
description: Die ADsOpenObject-Funktion und die IADsOpenDSObject OpenDSObject-Methode werden verwendet, um eine Bindung an Verzeichnisdienstobjekte zu erstellen, wenn alternative Anmeldeinformationen angegeben werden müssen und datenverschlüsselung erforderlich ist.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Binden mit ADsOpenObject und IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI , verwenden, binden mit ADsOpenObject und IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41ffe1e9ad0b8a78d1a8c563de250851a894012938682c4cfd0d0fd713f99bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082774"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Binden mit ADsOpenObject und IADsOpenDSObject::OpenDSObject

Die [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und die [**IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) werden verwendet, um eine Bindung an Verzeichnisdienstobjekte durchzuführen, wenn alternative Anmeldeinformationen angegeben werden müssen und datenverschlüsselung erforderlich ist.

Die Anmeldeinformationen des aufrufenden Threads sollten nach Möglichkeit verwendet werden. Wenn jedoch alternative Anmeldeinformationen verwendet werden müssen, müssen die [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder die [**IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) verwendet werden. Wenn alternative Anmeldeinformationen verwendet werden, ist es wichtig, das Kennwort nicht zwischenzuspeichern. Mehrere Bindungsvorgänge können ausgeführt werden, indem Der Benutzername und das Kennwort für den ersten Bindungsvorgang und dann nur der Benutzername in nachfolgenden Bindungen angegeben werden. Das System richtet eine Sitzung beim ersten Aufruf ein und verwendet dieselbe Sitzung für nachfolgende Bindungsaufrufe, solange die folgenden Bedingungen erfüllt sind:

-   Der gleiche Benutzername in jedem Bindungsvorgang.
-   Implementieren Sie bei jedem Bindungsvorgang eine serverlose Bindung oder bindung an denselben Server.
-   Verwalten Sie eine geöffnete Sitzung, indem Sie einen Objektverweis aus einem der Bindungsvorgänge beibehalten. Die Sitzung wird geschlossen, wenn der letzte Objektverweis freigegeben wird.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) verwenden die Windows NT [Security Support Provider Interfaces (SSPI),](/windows/desktop/SecAuthN/sspi) um Flexibilität bei den Authentifizierungsoptionen zu ermöglichen. Der Hauptvorteil der Verwendung dieser Schnittstellen besteht darin, verschiedene Authentifizierungstypen für Active Directory-Clients bereitzustellen und die Sitzung zu verschlüsseln. Derzeit lässt ADSI nicht zu, dass Zertifikate übergeben werden. Daher können Sie SSL für die Verschlüsselung und dann Kerberos, NTLM oder die einfache Authentifizierung verwenden, je nachdem, wie die Flags für den *dwReserved-Parameter* festgelegt werden.

Sie können keinen bestimmten SSPI-Anbieter in ADSI anfordern, obwohl Sie immer das Protokoll mit der höchsten Präferenz erhalten. Im Fall einer Windows Clientbindung an einen Computer, auf dem Windows ausgeführt wird, ist das Protokoll Kerberos. Das Zulassen eines Zertifikats für die Authentifizierung ist im Fall einer Webseite akzeptabel, da die Authentifizierung vor dem Ausführen der Webseite erfolgt.

Obwohl Open-Vorgänge es Ihnen ermöglichen, einen Benutzer und ein Kennwort anzugeben, sollten Sie dies nicht tun. Geben Sie stattdessen keine Anmeldeinformationen an, und verwenden Sie implizit die Anmeldeinformationen des Sicherheitskontexts des Aufrufers. Um eine Bindung an ein Verzeichnisobjekt mithilfe der Anmeldeinformationen des Aufrufers mit [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)zu erstellen, geben Sie **NULL** für Benutzername und Kennwort an.

Verwenden Sie abschließend das ADS **\_ NO \_ AUTHENTICATION-Flag,** um eine Bindung ohne Authentifizierung durchzuführen. Keine Authentifizierung gibt an, dass ADSI versucht, als anonymer Benutzer an das Zielobjekt zu binden, und führt keine Authentifizierung durch. Dies entspricht der Anforderung anonymer Bindungen in LDAP und gibt an, dass alle Benutzer im Sicherheitskontext enthalten sind.

Wenn die Authentifizierungsflags auf 0 (null) festgelegt sind, führt ADSI eine einfache Bindung aus, die als Klartext gesendet wird.

> [!Caution]  
> Wenn ein Benutzername und ein Kennwort ohne Angabe von Authentifizierungsflags angegeben werden, werden Benutzername und Kennwort in Klartext über das Netzwerk übertragen, was ein Sicherheitsrisiko darstellt. Geben Sie keinen Benutzernamen und kein Kennwort an, ohne Authentifizierungsflags anzugeben.

 

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird die Verwendung der [**IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) veranschaulicht.


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



Im folgenden C++-Codebeispiel wird die Verwendung der [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) veranschaulicht.


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



Die [**IADsOpenDSObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) kann auch in C++ verwendet werden, dupliziert jedoch die [**ADsOpenObject-Funktion.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

Das folgende C++-Codebeispiel zeigt, wie Sie die [**IADsOpenDSObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) verwenden, um den gleichen Bindungsvorgang wie im obigen Codebeispiel auszuführen.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 