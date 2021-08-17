---
description: Erläutert die Verwendung der SSPI-Nachrichtenunterstützung.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Verwenden der Nachrichtenunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c6a14c28cc9eb9e1b606574659412a22f375ad935ee0d7d1bdd898781c230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785920"
---
# <a name="using-message-support"></a>Verwenden der Nachrichtenunterstützung

Nachdem ein Handshake abgeschlossen und eine sichere Verbindung hergestellt wurde, kann eine Anwendung die Funktionen [**MakeSignature,**](/windows/desktop/api/Sspi/nf-sspi-makesignature) [**EncryptMessage (Allgemein),**](/windows/win32/api/sspi/nf-sspi-encryptmessage) [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)und [**DecryptMessage (Allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) verwenden, um signierte oder verschlüsselte Anwendungsdaten mit dem Remotecomputer auszutauschen.

Beispiele, die diese Funktionen verwenden, nachdem ein [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, werden in den folgenden Abschnitten veranschaulicht:

-   [Signieren einer Nachricht](signing-a-message.md)
-   [Überprüfen einer Nachricht](verifying-a-message.md)
-   [Verschlüsseln einer Nachricht](encrypting-a-message.md)
-   [Entschlüsseln einer Nachricht](decrypting-a-message.md)

 

 
