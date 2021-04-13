---
title: COM-Sicherheitsstandards
description: Sie können die com-Sicherheits Standardwerte für Ihre Anwendung verwenden, anstatt eigene Sicherheitseinstellungen anzugeben.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309292"
---
# <a name="com-security-defaults"></a>COM-Sicherheitsstandards

Sie können die com-Sicherheits Standardwerte für Ihre Anwendung verwenden, anstatt eigene Sicherheitseinstellungen anzugeben. In diesem Fall wird die Sicherheit von com initialisiert und verwaltet. Sie müssen die Registrierung nicht konfigurieren oder keine Sicherheitsfunktionen in Ihrem Programm abrufen.

Wenn jedoch bestimmte Registrierungs Werte festgelegt oder geändert wurden, wirkt sich dies auf die Sicherheitsstandards aus, die von com verwendet werden. In der folgenden Liste werden die Standardwerte für COM-Sicherheit beschrieben und erläutert, wie einige Werte durch Registrierungs Einstellungen beeinflusst werden.

Im folgenden sind die von com verwendeten Standard Sicherheitswerte aufgeführt:

-   Der Standard-Sicherheits Dienstanbieter ist der von com festgelegte, der am meisten mit der-Umgebung kompatibel ist. COM wählt entweder das Kerberos V5-Protokoll oder NTLMSSP aus, wobei das Kerberos-Protokoll die Standardauswahl ist. Keines der Protokolle, die von SChannel bereitgestellt werden, wird jemals als Standard ausgewählt.
-   Das System identifiziert einen Aufrufer über den Benutzernamen und das Kennwort und erstellt automatisch ein Identifizierungs Token, das vom Sicherheitssystem verwendet wird.
-   Wenn der benannte Wert " [legacyauthenticationlevel](legacyauthenticationlevel.md) " vorhanden ist und der Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Authentifizierungs Ebene bei Connect (RPC- \_ C- \_ authn \_ Level \_ Connect) festgelegt. Diese Ebene bedeutet, dass bei dem ersten-Client, der einen Client an den Server sendet, com eine Authentifizierungs Überprüfung ausführt. Wenn der Client die Überprüfung übergibt, erfolgt keine weitere Authentifizierung. Der AuthenticationLevel-Wert kann auch unter dem Schlüssel " [AppID](appid-key.md) " festgelegt werden.
-   Wenn der benannte Wert von " [legacyidentitäts ationlevel](legacyimpersonationlevel.md) " vorhanden ist und der Wert festgelegt wurde, wird dieser Wert verwendet. Andernfalls wird die Identitätswechsel Ebene auf "identifizieren" festgelegt (RPC \_ C \_ IMP- \_ Ebene \_ identifizieren). Dem Server werden Identitätswechsel Rechte vom Client erteilt. Die Ebene "identifizieren" bedeutet, dass der Server die Identität des Clients abrufen kann. Der Server kann die Identität des Clients für die Überprüfung der Zugriffs Steuerungs Liste (ACL) annehmen, aber nicht als Client auf Systemobjekte zugreifen. Weitere Informationen finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und [Cloaking](cloaking.md).
-   Wenn der benannte Wert [AccessPermission](accesspermission.md) unter **AppID** vorhanden und festgelegt wurde, wird dieser Wert verwendet. Andernfalls prüft com einen [DefaultAccessPermission](defaultaccesspermission.md) -Eintrag. Falls vorhanden, wird dieser Wert verwendet. Wenn dieser Wert nicht vorhanden ist, erstellt com eine ACL, die Berechtigungen für die Server Identität und das lokale System erteilt.
-   Wenn der benannte Wert [SRPTrustLevel](srptrustlevel.md) unter **AppID** vorhanden und festgelegt wurde, wird dieser Wert verwendet. Andernfalls ist die Richtlinie für die Software Einschränkungs Richtlinie (SRP) auf unzulässig (sicherere \_ levelid unzulässig) festgelegt \_ , was darauf hinweist, dass die Anwendung in einer eingeschränkten Umgebung ausgeführt wird und für den Zugriff auf sicherheitsrelevante Benutzerberechtigungen des Benutzers nicht zulässig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




