---
title: COM-Sicherheitseinstellungen
description: Sie können die COM-Sichten für Ihre Anwendung verwenden, anstatt Ihre eigenen Sicherheitseinstellungen anzugeben.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6287e00971eca3afe94e598555225943709d1c42546fccb76a442a0dfe3be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550595"
---
# <a name="com-security-defaults"></a>COM-Sicherheitseinstellungen

Sie können die COM-Sichten für Ihre Anwendung verwenden, anstatt Ihre eigenen Sicherheitseinstellungen anzugeben. In diesem Fall initialisiert und verwaltet COM die Sicherheit für Sie. Sie müssen die Registrierung nicht konfigurieren oder Sicherheitsfunktionen in Ihrem Programm aufrufen.

Wenn jedoch bestimmte benannte Registrierungswerte festgelegt oder geändert wurden, sind die von COM verwendeten Sichten betroffen. In der folgenden Liste werden die Standardwerte für die COM-Sicherheit beschrieben, und es wird erläutert, wie einige Werte durch Registrierungseinstellungen beeinflusst werden.

Im Folgenden finden Sie die Von COM verwendeten Standardsicherheitswerte:

-   Der Standardmäßige Sicherheitsdienstanbieter ist der, der von COM als der mit der Umgebung am kompatibelsten bestimmt wird. COM wählt entweder das Kerberos v5-Protokoll oder NTLMSSP aus, und das Kerberos-Protokoll ist die Standardauswahl. Keines der von Schannel bereitgestellten Protokolle wird jemals als Standard ausgewählt.
-   Das System identifiziert einen Aufrufer über Benutzername und Kennwort und erstellt automatisch ein Vom Sicherheitssystem verwendetes Identifikationstoken.
-   Wenn der [benannte Wert LegacyAuthenticationLevel](legacyauthenticationlevel.md) vorhanden ist und sein Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Authentifizierungsebene auf Connect festgelegt (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT). Diese Ebene bedeutet, dass COM beim ersten Aufruf, den ein Client an den Server sendet, eine Authentifizierungsprüfung vorn hat. Wenn der Client die Überprüfung besteht, erfolgt keine weitere Authentifizierung. Der AuthenticationLevel-Wert kann auch unter dem [AppID-Schlüssel festgelegt](appid-key.md) werden.
-   Wenn der [benannte Wert LegacyImpersonationLevel](legacyimpersonationlevel.md) vorhanden ist und sein Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Identitätswechselebene auf identify (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY) festgelegt. Identitätswechselrechte werden dem Server vom Client gewährt. Die Identifizierungsebene bedeutet, dass der Server die Identität des Clients abrufen kann. Der Server kann die Identität des Clients für die Überprüfung der Zugriffssteuerungsliste (Access Control List, ACL) imitieren, aber nicht auf Systemobjekte als Client zugreifen. Weitere Informationen finden Sie unter [Identitätswechselebenen](impersonation-levels.md) und [Cloaking](cloaking.md).
-   Wenn der [benannte AccessPermission-Wert](accesspermission.md) unter **AppID** vorhanden ist und festgelegt wurde, wird dieser Wert verwendet. Andernfalls sucht COM nach einem [DefaultAccessPermission-Eintrag.](defaultaccesspermission.md) Falls vorhanden, wird dieser Wert verwendet. Wenn dieser Wert nicht vorhanden ist, erstellt COM eine ACL, die Berechtigungen für die Serveridentität und das lokale System gewährt.
-   Wenn der [benannte Wert SRPTrustLevel](srptrustlevel.md) unter **AppID** vorhanden ist und festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Vertrauensebene der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) auf Disallowed (SAFER \_ LEVELID DISALLOWED) festgelegt. Dies bedeutet, dass die Anwendung in einer eingeschränkten Umgebung ausgeführt wird und nicht auf sicherheitsempfindliche Benutzerberechtigungen des Benutzers \_ zugreifen kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




