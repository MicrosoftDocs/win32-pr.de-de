---
title: Binden mit GetObject und ADsGetObject
description: Die Funktionen "GetObject" und "ADsGetObject" werden zum Binden an Verzeichnisdienst Objekte ohne Authentifizierung verwendet.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindung mit GetObject und ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949102"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Binden mit GetObject und ADsGetObject

Die Funktionen " **GetObject** " und " [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) " werden zum Binden an Verzeichnisdienst Objekte ohne Authentifizierung verwendet. Die Anwendung muss beim Zugriff auf die Verzeichnisdienst Daten keine Anmelde Informationen bereitstellen. ADSI verwendet den Sicherheitskontext des aufrufenden Threads. Wenn die sichere Authentifizierung jedoch fehlschlägt, versucht ADSI, eine einfache Bindung mit einem NULL-Benutzernamen und einem NULL-Kennwort auszuführen. Wenn die einfache Bindung erfolgreich ist, ist der Benutzer Kontext für die Bindung Guest. Eine einfache Bindung verwendet Klartext-Authentifizierung. Da kein Benutzername oder Kennwort über das Netzwerk übertragen wird, ist dies kein Sicherheitsproblem.

Die **GetObject** -Funktion wird zum Binden an Verzeichnisdienst Objekte in Sprachen verwendet, die Automation unterstützen, z. b. Visual Basic. Die **GetObject** -Funktion erfordert eine Monikerzeichenfolge. In ADSI ist die Bindungs Zeichenfolge die Monikerzeichenfolge.

In Sprachen, die Automation nicht direkt unterstützen, wie z. b. C oder C++, stellt ADSI die [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Funktion für die Bindung an Verzeichnisdienst Objekte bereit. Alternativ können die Funktionen " [**mktisedisplayname**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) " und " [**mkparamesedisplaynameex**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " verwendet werden, um das gleiche Ergebnis wie " **GetObject**" zu erzielen.

Für einen Dienst, der unter dem Konto "LocalSystem" ausgeführt wird, hängt der von **GetObject** und [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) verwendete Sicherheitskontext von dem Computer ab, auf dem der Dienst ausgeführt wird. Wenn der Dienst auf einem Domänen Controller als "LocalSystem" ausgeführt wird, verfügt der Dienst über vollständigen Zugriff auf die Systemebene auf Active Directory. Wenn der Dienst nicht auf einem Domänen Controller ausgeführt wird, verfügt der Dienst über die Zugriffsrechte und-Berechtigungen, die dem Computer Konto für den Computer gewährt werden, auf dem der Dienst ausgeführt wird. Dies ist erheblich weniger leistungsfähiger als der Zugriff auf Systemebene.

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird gezeigt, wie die **GetObject** -Funktion verwendet wird, um eine Bindung an ein-Objekt herzustellen.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



Im folgenden C++-Codebeispiel wird gezeigt, wie die [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Funktion verwendet wird, um eine Bindung an ein-Objekt herzustellen.


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



 

 