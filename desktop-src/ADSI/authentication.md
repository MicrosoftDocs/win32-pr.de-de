---
title: Authentifizierung (ADSI)
description: In ADSI werden Anmeldeinformationen, die aus einem Benutzernamen und kennwort bestehen, verwendet, um den Zugriff auf Objekte im Verzeichnisdienst zu ermöglichen oder einzuschränken.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI-Authentifizierung
- ADSI, Using, Authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840557"
---
# <a name="authentication-adsi"></a>Authentifizierung (ADSI)

In ADSI werden Anmeldeinformationen, die aus einem Benutzernamen und kennwort bestehen, verwendet, um den Zugriff auf Objekte im Verzeichnisdienst zu ermöglichen oder einzuschränken. Die [**ADsGetObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) verwendet die Anmeldeinformationen des aufrufenden Threads für die Authentifizierung. Die [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und [**die IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) können verwendet werden, um andere Anmeldeinformationen als die des aufrufenden Threads anzugeben. Wenn ein Objekt mit einem authentifizierten Benutzer an gebunden ist, wird dem Benutzer der Zugriff auf das Objekt gestattet, wie von den zugrunde liegenden Sicherheitsanforderungen des Verzeichnisdiensts unterstützt.

> [!Note]  
> Die [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und [**die IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) sollten nicht zum Überprüfen von Benutzeranmeldeinformationen verwendet werden. Weitere Informationen zum Überprüfen von Benutzeranmeldeinformationen finden Sie im Microsoft Knowledge Base artikel 180548 HOWTO: Validate User Credentials on Microsoft Operating Systems (Überprüfen von Benutzeranmeldeinformationen unter [Microsoft-Betriebssystemen).](https://support.microsoft.com/kb/180548)

 

Das folgende Codebeispiel zeigt, wie Sie die [**OpenDSObject-Methode verwenden,**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) um einen Benutzer zu authentifizieren.


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



 

 




