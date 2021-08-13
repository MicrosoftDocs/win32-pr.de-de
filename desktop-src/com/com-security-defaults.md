---
title: COM-Sicherheitsstandards
description: Sie können die COM-Sicherheitsstandards für Ihre Anwendung verwenden, anstatt Ihre eigenen Sicherheitseinstellungen anzugeben.
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
# <a name="com-security-defaults"></a>COM-Sicherheitsstandards

Sie können die COM-Sicherheitsstandards für Ihre Anwendung verwenden, anstatt Ihre eigenen Sicherheitseinstellungen anzugeben. In diesem Fall initialisiert UND verwaltet COM die Sicherheit für Sie. Sie müssen die Registrierung nicht konfigurieren oder Sicherheitsfunktionen in Ihrem Programm aufrufen.

Wenn jedoch bestimmte benannte Registrierungswerte festgelegt oder geändert wurden, sind die von COM verwendeten Sicherheitsstandards betroffen. In der folgenden Liste werden die COM-Sicherheitsstandardwerte beschrieben und erläutert, wie einige Werte durch Registrierungseinstellungen beeinflusst werden.

Im Folgenden sind die Von COM verwendeten Standardsicherheitswerte angegeben:

-   Der Standardsicherheitsdienstanbieter wird von COM als der mit der Umgebung am besten kompatible Anbieter festgelegt. COM wählt entweder das Kerberos v5-Protokoll oder NTLMSSP aus, wobei das Kerberos-Protokoll die Standardauswahl ist. Keines der von Schannel bereitgestellten Protokolle wird jemals als Standard ausgewählt.
-   Das System identifiziert einen Aufrufer über Benutzername und Kennwort und erstellt automatisch ein vom Sicherheitssystem verwendetes Identifikationstoken.
-   Wenn der benannte Wert [LegacyAuthenticationLevel](legacyauthenticationlevel.md) vorhanden ist und sein Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Authentifizierungsebene auf connect (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT) festgelegt. Diese Ebene bedeutet, dass com beim ersten Aufruf eines Clients an den Server eine Authentifizierungsprüfung vornimmt. Wenn der Client die Überprüfung besteht, erfolgt keine weitere Authentifizierung. Der AuthenticationLevel-Wert kann auch unter dem [AppID-Schlüssel](appid-key.md) festgelegt werden.
-   Wenn der [LegacyImpersonationLevel-Wert](legacyimpersonationlevel.md) vorhanden ist und sein Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Identitätswechselebene auf identify festgelegt (RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY). Identitätswechselrechte werden vom Client dem Server gewährt. Die Identifizierungsebene bedeutet, dass der Server die Identität des Clients abrufen kann. Der Server kann die Identität des Clients für die Überprüfung der Zugriffssteuerungsliste (Access Control List, ACL) annehmen, aber nicht als Client auf Systemobjekte zugreifen. Weitere Informationen finden Sie unter [Identitätswechselebenen](impersonation-levels.md) und [Verleumden von](cloaking.md).
-   Wenn der benannte [AccessPermission-Wert](accesspermission.md) unter **AppID** vorhanden ist und festgelegt wurde, wird dieser Wert verwendet. Andernfalls sucht COM nach einem [DefaultAccessPermission-Eintrag.](defaultaccesspermission.md) Falls vorhanden, wird dieser Wert verwendet. Wenn dieser Wert nicht vorhanden ist, erstellt COM eine Zugriffssteuerungsliste, die Berechtigungen für die Serveridentität und das lokale System gewährt.
-   Wenn der benannte [SRPTrustLevel-Wert](srptrustlevel.md) unter **AppID** vorhanden ist und festgelegt wurde, wird dieser Wert verwendet. Andernfalls ist die Vertrauensebene der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) auf Nicht zulässig (SAFER \_ LEVELID \_ DISALLOWED) festgelegt. Dies gibt an, dass die Anwendung in einer eingeschränkten Umgebung ausgeführt wird und nicht auf sicherheitsbezogene Benutzerberechtigungen des Benutzers zugreifen darf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




