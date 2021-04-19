---
description: Erläutert, wie SChannel-Anmelde Informationen manuell überprüft werden.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Manuelles Überprüfen von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363634"
---
# <a name="manually-validating-schannel-credentials"></a>Manuelles Überprüfen von SChannel-Anmelde Informationen

Standardmäßig überprüft SChannel das [*Serverzertifikat*](../secgloss/s-gly.md) durch Aufrufen der [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) -Funktion. Wenn Sie diese Funktion jedoch mit dem Flag für die manuelle Initialisierung von "ISC req" deaktiviert haben \_ \_ \_ \_ , müssen Sie das Zertifikat überprüfen, das von dem Server bereitgestellt wird, der versucht, seine Identität zu ermitteln.

Wenn Sie das Serverzertifikat manuell überprüfen möchten, müssen Sie es zuerst erhalten. Verwenden Sie die Funktion [**QueryContextAttributes (allgemein)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) , und geben Sie den Wert des Attributs "secpkg \_ attr \_ Remote \_ CERT Context" an \_ . Dieses Attribut gibt eine [**CERT- \_ Kontext**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Struktur zurück, die das vom Server bereitgestellte Zertifikat enthält. Dieses Zertifikat wird als Blatt Zertifikat bezeichnet, da es das letzte Zertifikat in der Zertifikat Kette ist und vom Stamm [*Zertifikat*](../secgloss/r-gly.md)entfernt ist.

Mithilfe des Blatt Zertifikats müssen Sie Folgendes überprüfen:

-   Die Zertifikatskette ist fertiggestellt, und der Stamm ist ein Zertifikat von einer vertrauenswürdigen Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca).
-   Die aktuelle Zeit liegt nicht außerhalb des Anfangs-und Enddatums für jedes der Zertifikate in der Zertifikatskette.
-   Keines der Zertifikate in der Zertifikat Kette wurde widerrufen.
-   Die Tiefe des Blatt Zertifikats ist nicht tiefer als die maximale zulässige Tiefe, die in der Zertifikat Erweiterung angegeben ist. Diese Überprüfung ist nur erforderlich, wenn eine Tiefe angegeben ist.
-   Die Verwendung des Zertifikats ist korrekt, z. b., wenn ein [*Client Zertifikat*](../secgloss/c-gly.md) nicht zum Authentifizieren eines Servers verwendet werden soll.
-   Bei der Server Authentifizierung entspricht die Server Identität, die im Blatt Zertifikat des Servers enthalten ist, dem Server, mit dem der Client eine Verbindung herzustellen versucht. In der Regel wird der Client ein Element im Feld "Antragsteller Name" des Zertifikats mit der IP-Adresse oder dem DNS-Namen des Servers vergleichen.

 

 
