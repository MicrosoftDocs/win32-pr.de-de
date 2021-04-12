---
title: Authentifizierung (ADSI)
description: In ADSI werden Anmelde Informationen, die aus einem Benutzernamen und einem Kennwort bestehen, verwendet, um den Zugriff auf Objekte im Verzeichnisdienst bereitzustellen oder einzuschränken.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- Authentifizierungsadsi
- ADSI, using, Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472276"
---
# <a name="authentication-adsi"></a>Authentifizierung (ADSI)

In ADSI werden Anmelde Informationen, die aus einem Benutzernamen und einem Kennwort bestehen, verwendet, um den Zugriff auf Objekte im Verzeichnisdienst bereitzustellen oder einzuschränken. Die [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Funktion verwendet die Anmelde Informationen des aufrufenden Threads für die Authentifizierung. Die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion und die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode können verwendet werden, um andere Anmelde Informationen als die des aufrufenden Threads anzugeben. Wenn ein Objekt mit einem authentifizierten Benutzer an gebunden wird, wird dem Benutzer der Zugriff auf das Objekt gewährt, das von den zugrunde liegenden Sicherheitsanforderungen des Verzeichnis Diensts unterstützt wird.

> [!Note]  
> Die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion und die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode sollten nicht zum Überprüfen von Benutzer Anmelde Informationen verwendet werden. Weitere Informationen zum Überprüfen von Benutzer Anmelde Informationen finden Sie im Microsoft Knowledge Base-Artikel 180548 [HOWTO: Überprüfen von Benutzer Anmelde Informationen auf Microsoft-Betriebssystemen](https://support.microsoft.com/kb/180548).

 

Im folgenden Codebeispiel wird gezeigt, wie die [**opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode verwendet wird, um einen Benutzer zu authentifizieren.


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




