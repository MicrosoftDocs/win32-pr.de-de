---
description: Alle SChannel-Protokolle erfordern, dass der Server ein Zertifikat von einer vertrauenswürdigen Zertifizierungsstelle (Certification Authority, ca) als Nachweis seiner Identität bereitstellt.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Durchführen der Authentifizierung mithilfe von SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a37b8dedf07680286288234c7ca4422f44c2c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356191"
---
# <a name="performing-authentication-using-schannel"></a>Durchführen der Authentifizierung mithilfe von SChannel

Alle SChannel-Protokolle erfordern, dass der Server ein [*Zertifikat*](../secgloss/c-gly.md) von einer vertrauenswürdigen Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) als Nachweis seiner Identität bereitstellt. Dieser Vorgang wird als Server Authentifizierung bezeichnet. Die Client Authentifizierung, bei der der Client einen Nachweis seiner Identität bereitstellt, ist optional und kann vom Server jederzeit angefordert werden.

## <a name="authenticating-the-server"></a>Authentifizieren des Servers

Das Standardverhalten von SChannel besteht darin, die [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) -Funktion zu verwenden, um die [*Integrität*](../secgloss/i-gly.md) und den Besitz des [*Serverzertifikats*](../secgloss/s-gly.md)zu überprüfen. Wenn Sie diese Funktion deaktivieren möchten, geben Sie \_ \_ \_ \_ beim Aufrufen der [**InitializeSecurityContext-Funktion (SChannel)**](./initializesecuritycontext--schannel.md) die "ISC req Manual cred Validation" an. Weitere Informationen finden Sie unter [Manuelles Validieren von SChannel-Anmelde](manually-validating-schannel-credentials.md)Informationen.

## <a name="authenticating-the-client"></a>Authentifizieren des Clients

SChannel überprüft nicht die Zertifikate des Clients. der Server muss diese Authentifizierung manuell ausführen. In der Regel überprüft der Server die Identität des Clients in einer Datenbank, die Benutzerkontoinformationen enthält. Für Server, die ein Client Konto mithilfe eines Zertifikats abrufen müssen, finden Sie weitere Informationen unter [Mapping von Zertifikaten](mapping-certificates.md).

Wenn der Server die Client Authentifizierung anfordert, muss der Client den Server eines seiner Zertifikate senden. Standardmäßig versucht SChannel ohne Benachrichtigung an den Client, ein [*Client Zertifikat*](../secgloss/c-gly.md) zu finden und an den Server zu senden. Um dieses Feature zu deaktivieren, geben Clients \_ die von ISC req \_ verwendete Verwendung von \_ creds an, \_ Wenn Sie die Funktion [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) aufrufen. Wenn dieses Flag angegeben wird, gibt SChannel \_ \_ \_ die Anmelde Informationen für den Client nicht unvollständig an den Client zurück, wenn der Server die Authentifizierung anfordert und der Client zuvor noch kein Zertifikat bereitgestellt hat.

 

 
