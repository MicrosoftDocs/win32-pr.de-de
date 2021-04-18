---
description: Erläutert die Verwendung der SSPI-Nachrichten Unterstützung.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Verwenden der Nachrichten Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352230"
---
# <a name="using-message-support"></a>Verwenden der Nachrichten Unterstützung

Nachdem ein Hand Shake Vorgang abgeschlossen und eine sichere Verbindung hergestellt wurde, kann eine Anwendung die Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**verschlüsseltmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) zum Austauschen von signierten oder verschlüsselten Anwendungsdaten mit dem Remote Computer verwenden.

Beispiele, die diese Funktionen verwenden, nachdem ein [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, werden in den folgenden Abschnitten veranschaulicht:

-   [Signieren einer Nachricht](signing-a-message.md)
-   [Überprüfen einer Nachricht](verifying-a-message.md)
-   [Verschlüsseln einer Nachricht](encrypting-a-message.md)
-   [Entschlüsseln einer Nachricht](decrypting-a-message.md)

 

 
