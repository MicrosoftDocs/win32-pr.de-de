---
title: Binden mit ADsOpenObject und iadsopendsobject opendsobject
description: Die ADsOpenObject-Funktion und die iadsopendsobject opendsobject-Methode werden zum Binden an Verzeichnisdienst Objekte verwendet, wenn alternative Anmelde Informationen angegeben werden müssen und die Datenverschlüsselung erforderlich ist.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Binden mit ADsOpenObject und iadsopendsobject opendsobject ADSI
- ADSI ADSI, using, Bindung mit ADsOpenObject und iadsopendsobject opendsobject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039600"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Binden mit ADsOpenObject und iadsopendsobject:: opendsobject

Die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion und die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode werden zum Binden an Verzeichnisdienst Objekte verwendet, wenn alternative Anmelde Informationen angegeben werden müssen und die Datenverschlüsselung erforderlich ist.

Wenn möglich, sollten die Anmelde Informationen des aufrufenden Threads verwendet werden. Wenn jedoch alternative Anmelde Informationen verwendet werden müssen, muss die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion oder die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode verwendet werden. Wenn Alternative Anmelde Informationen verwendet werden, ist es wichtig, das Kennwort nicht zwischenzuspeichern. Mehrere Bindungs Vorgänge können ausgeführt werden, indem Sie den Benutzernamen und das Kennwort für den ersten Bindungs Vorgang angeben und dann nur den Benutzernamen in nachfolgenden Bindungen angeben. Das System richtet eine Sitzung beim ersten Aufruf ein und verwendet dieselbe Sitzung bei nachfolgenden Bindungs aufrufen, solange die folgenden Bedingungen erfüllt sind:

-   Derselbe Benutzername in jedem Bindungs Vorgang.
-   Implementieren Sie in jedem Bindungs Vorgang eine Server lose Bindung oder eine Bindung an denselben Server.
-   Warten Sie eine offene Sitzung, indem Sie einen Objekt Verweis von einem der Bindungs Vorgänge an einem Objekt Verweis halten. Die Sitzung wird geschlossen, wenn der letzte Objekt Verweis freigegeben wird.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) verwenden die Windows NT [Security Support Provider-Schnittstellen (SSPI)](/windows/desktop/SecAuthN/sspi) , um Flexibilität bei Authentifizierungs Optionen zu ermöglichen. Der Hauptvorteil der Verwendung dieser Schnittstellen besteht darin, den Active Directory Clients verschiedene Authentifizierungs Typen bereitzustellen und die Sitzung zu verschlüsseln. Derzeit lässt ADSI nicht zu, dass Zertifikate übermittelt werden. Daher können Sie SSL für die Verschlüsselung und dann die Kerberos-, NTLM-oder einfache Authentifizierung verwenden. Dies hängt davon ab, wie die Flags für den *dwReserved* -Parameter festgelegt werden.

Es ist nicht möglich, einen bestimmten SSPI-Anbieter in ADSI anzufordern, obwohl Sie immer das höchste bevorzugte Protokoll erhalten. Bei einer Windows-Client Bindung an einen Computer, auf dem Windows ausgeführt wird, ist das Protokoll Kerberos. Das zulassen eines Zertifikats für die Authentifizierung ist im Fall einer Webseite akzeptabel, da die Authentifizierung vor dem Ausführen der Webseite erfolgt.

Obwohl Sie mit offenen Vorgängen einen Benutzer und ein Kennwort angeben können, sollten Sie dies nicht tun. Geben Sie stattdessen keine Anmelde Informationen an, und verwenden Sie implizit die Anmelde Informationen des Sicherheits Kontexts des Aufrufers. Geben Sie für den Benutzernamen und das Kennwort **null** an, um die Bindung an ein Verzeichnis Objekt mithilfe der Anmelde Informationen des Aufrufers mit [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)herzustellen.

Zum Binden ohne Authentifizierung verwenden Sie schließlich das Flag **ADS \_ No \_ Authentication** . Keine Authentifizierung gibt an, dass ADSI versucht, als anonymer Benutzer an das Zielobjekt zu binden, und führt keine Authentifizierung durch. Dies entspricht der Anforderung der anonymen Bindung in LDAP und gibt an, dass alle Benutzer im Sicherheitskontext enthalten sind.

Wenn die Authentifizierungsflags auf NULL festgelegt sind, führt ADSI eine einfache Bindung aus, die als Klartext gesendet wird.

> [!Caution]  
> Wenn ein Benutzername und ein Kennwort ohne Angabe von Authentifizierungsflags angegeben werden, werden der Benutzername und das Kennwort im Klartext über das Netzwerk übertragen, was ein Sicherheitsrisiko darstellt. Geben Sie keinen Benutzernamen und kein Kennwort an, ohne Authentifizierungsflags anzugeben.

 

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird die Verwendung der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode veranschaulicht.


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



Im folgenden C++-Codebeispiel wird die Verwendung der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion veranschaulicht.


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



Die [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) -Schnittstelle kann auch in C++ verwendet werden, aber die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion wird dupliziert.

Im folgenden C++-Codebeispiel wird gezeigt, wie die [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) -Schnittstelle verwendet wird, um denselben Bindungs Vorgang wie im obigen Codebeispiel auszuführen.


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



 

 