---
description: Erläutert, wie Schannel-Anmeldeinformationen manuell überprüft werden.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Manuelles Überprüfen von Schannel-Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71ddff50ab674825d8effd1a08477116ee0c654d031e7f353a30c95e4f1249f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787002"
---
# <a name="manually-validating-schannel-credentials"></a>Manuelles Überprüfen von Schannel-Anmeldeinformationen

Standardmäßig überprüft Schannel das [*Serverzertifikat,*](../secgloss/s-gly.md) indem die [**WinVerifyTrust-Funktion**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) aufgerufen wird. Wenn Sie dieses Feature jedoch mithilfe des ISC \_ REQ \_ MANUAL \_ CRED \_ VALIDATION-Flags deaktiviert haben, müssen Sie das vom Server bereitgestellte Zertifikat überprüfen, der versucht, seine Identität herzustellen.

Um das Serverzertifikat manuell zu überprüfen, müssen Sie es zuerst abrufen. Verwenden Sie die [**QueryContextAttributes (General)-Funktion,**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) und geben Sie den SECPKG \_ ATTR \_ REMOTE \_ CERT \_ CONTEXT-Attributwert an. Dieses Attribut gibt eine [**CERT \_ CONTEXT-Struktur**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) zurück, die das vom Server bereitgestellte Zertifikat enthält. Dieses Zertifikat wird als Blattzertifikat bezeichnet, da es das letzte Zertifikat in der Zertifikatkette ist und am weitesten vom [*Stammzertifikat*](../secgloss/r-gly.md)entfernt ist.

Mithilfe des Blattzertifikats müssen Sie Folgendes überprüfen:

-   Die Zertifikatkette ist vollständig, und der Stamm ist ein Zertifikat einer vertrauenswürdigen [*Zertifizierungsstelle.*](../secgloss/c-gly.md)
-   Die aktuelle Zeit liegt nicht über dem Anfangs- und Enddatum für jedes Zertifikat in der Zertifikatkette hinaus.
-   Keines der Zertifikate in der Zertifikatkette wurde widerrufen.
-   Die Tiefe des Blattzertifikats liegt nicht tiefer als die maximal zulässige Tiefe, die in der Zertifikaterweiterung angegeben ist. Diese Überprüfung ist nur erforderlich, wenn eine Tiefe angegeben ist.
-   Die Verwendung des Zertifikats ist richtig. Ein [*Clientzertifikat*](../secgloss/c-gly.md) sollte beispielsweise nicht zum Authentifizieren eines Servers verwendet werden.
-   Bei der Serverauthentifizierung stimmt die im Blattzertifikat des Servers enthaltene Serveridentität mit dem Server überein, den der Client zu kontaktieren versucht. In der Regel stimmt der Client ein Element im Feld Antragstellername des Zertifikats mit der IP-Adresse oder dem DNS-Namen des Servers überein.

 

 
