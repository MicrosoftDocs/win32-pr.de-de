---
description: Alle Schannel-Protokolle erfordern, dass der Server ein Zertifikat von einer vertrauenswürdigen Zertifizierungsstelle als Nachweis seiner Identität bereitstellt.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Durchführen der Authentifizierung mithilfe von Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c2a5099dd29d6b3b342b583e37e2dc98187f5011c7cc75b75432924fba9ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921019"
---
# <a name="performing-authentication-using-schannel"></a>Durchführen der Authentifizierung mithilfe von Schannel

Alle Schannel-Protokolle erfordern, dass der Server ein [*Zertifikat*](../secgloss/c-gly.md) von einer vertrauenswürdigen [*Zertifizierungsstelle*](../secgloss/c-gly.md) als Nachweis seiner Identität bereitstellt. Dieser Prozess wird als Serverauthentifizierung bezeichnet. Die Clientauthentifizierung, bei der der Client einen Identitätsnachweis bereitstellt, ist optional und kann jederzeit vom Server angefordert werden.

## <a name="authenticating-the-server"></a>Authentifizieren des Servers

Das Standardverhalten von Schannel ist die Verwendung der [**WinVerifyTrust-Funktion,**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) um die [*Integrität*](../secgloss/i-gly.md) und den Besitz des [*Serverzertifikats*](../secgloss/s-gly.md)zu überprüfen. Um dieses Feature zu deaktivieren, geben Sie ISC \_ REQ \_ MANUAL \_ CRED \_ VALIDATION beim Aufrufen der [**InitializeSecurityContext (Schannel)-Funktion**](./initializesecuritycontext--schannel.md) an. Weitere Informationen finden Sie unter [Manuelles Überprüfen von Schannel-Anmeldeinformationen.](manually-validating-schannel-credentials.md)

## <a name="authenticating-the-client"></a>Authentifizieren des Clients

Schannel überprüft die Clientzertifikate nicht. Der Server muss diese Authentifizierung manuell ausführen. In der Regel überprüft der Server die Identität des Clients in einer Datenbank mit Benutzerkontoinformationen. Informationen zu Servern, die ein Clientkonto mithilfe eines Zertifikats abrufen müssen, finden Sie unter [Zuordnen von Zertifikaten.](mapping-certificates.md)

Wenn der Server die Clientauthentifizierung anfordert, muss der Client dem Server eines seiner Zertifikate senden. Standardmäßig versucht Schannel ohne Benachrichtigung an den Client, ein [*Clientzertifikat*](../secgloss/c-gly.md) zu finden und es an den Server zu senden. Um dieses Feature zu deaktivieren, geben Clients ISC \_ REQ \_ USE \_ SUPPLIED \_ CREDS beim Aufrufen der [**InitializeSecurityContext (Schannel)-Funktion**](./initializesecuritycontext--schannel.md) an. Wenn dieses Flag angegeben ist, gibt Schannel SEC \_ I \_ INCOMPLETE \_ CREDENTIALS an den Client zurück, wenn der Server die Authentifizierung anfordert und der Client zuvor kein Zertifikat bereitgestellt hat.

 

 
