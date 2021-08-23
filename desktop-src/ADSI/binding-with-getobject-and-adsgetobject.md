---
title: Binden mit GetObject und ADsGetObject
description: Die Funktionen GetObject und ADsGetObject werden verwendet, um ohne Authentifizierung an Verzeichnisdienstobjekte zu binden.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , using,binding mit GetObject und ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fe3f64368f6bbecf390d07f5258c11b6752badbf701e1f248439ca81428749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082754"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Binden mit GetObject und ADsGetObject

Die **Funktionen GetObject** und [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) werden verwendet, um ohne Authentifizierung an Verzeichnisdienstobjekte zu binden. Die Anwendung muss beim Zugriff auf Verzeichnisdienstdaten keine Anmeldeinformationen angeben. ADSI verwendet den Sicherheitskontext des aufrufenden Threads. Wenn bei der sicheren Authentifizierung jedoch ein Fehler auftritt, versucht ADSI, eine einfache Bindung mit einem NULL-Benutzernamen und NULL-Kennwort durchzuführen. Wenn die einfache Bindung erfolgreich ist, ist der Benutzerkontext für die Bindung Gast. Eine einfache Bindung verwendet die Klartextauthentifizierung. Da kein Benutzername oder Kennwort über das Netzwerk übertragen wird, ist dies kein Sicherheitsproblem.

Die **GetObject-Funktion** wird zum Binden an Verzeichnisdienstobjekte in Sprachen verwendet, die Automatisierung unterstützen, z. B. Visual Basic. Die **GetObject-Funktion** erfordert eine Monikerzeichenfolge. In ADSI ist die Bindungszeichenfolge die Monikerzeichenfolge.

In Sprachen, die die Automatisierung nicht direkt unterstützen, z. B. C oder C++, stellt ADSI die [**ADsGetObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) zum Binden an Verzeichnisdienstobjekte zur Verfügung. Alternativ können die [**Funktionen MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) und [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) verwendet werden, um das gleiche Ergebnis wie **GetObject zu erzielen.**

Bei einem Dienst, der unter dem LocalSystem-Konto ausgeführt wird, hängt der von **GetObject** und [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) verwendete Sicherheitskontext von dem Computer ab, auf dem der Dienst ausgeführt wird. Wenn der Dienst auf einem Domänencontroller als LocalSystem ausgeführt wird, verfügt der Dienst über vollständigen Zugriff auf Active Directory auf Systemebene. Wenn der Dienst nicht auf einem Domänencontroller ausgeführt wird, verfügt der Dienst über die Zugriffsrechte und Berechtigungen, die dem Computerkonto für den Computer gewährt werden, auf dem der Dienst ausgeführt wird. dies ist deutlich weniger leistungsfähig als der Zugriff auf Systemebene.

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird gezeigt, wie die **GetObject-Funktion** zum Binden an ein Objekt verwendet wird.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



Das folgende C++-Codebeispiel zeigt, wie die [**ADsGetObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) zum Binden an ein Objekt verwendet wird.


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 