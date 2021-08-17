---
description: Listet die Änderungen an den Funktionen signierter Daten auf.
ms.assetid: 0518a336-d996-4a82-9336-a448284c72dd
title: Ergänzungen signierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5e9f1433a432ba3c3a414e11b83e429ad9c0abc7364b5e5b7451f72d886e33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900390"
---
# <a name="signed-data-additions"></a>Ergänzungen signierter Daten

An den Funktionen für signierte Daten wurden die folgenden Änderungen vorgenommen:

-   Nichtdata [*innerer Inhalt*](../secgloss/i-gly.md) wird in einer OCTET-ZEICHENFOLGE gekapselt.
-   Die Bereitstellung erfolgt für verschiedene Nachrichtenversionen.
-   Signaturgeber können entweder anhand des Ausstellers und der Seriennummer (wie in PKCS 7 1.5) oder anhand des Schlüsselbezeichners \# des Betreffs identifiziert werden.
-   Mehrere Signierer sind zulässig.
-   Rsa-, DSA- und ECDSA-Signaturen sind zulässig.
-   ECC-basierte Algorithmen (Elliptic Curve Cryptography) und AES erfordern Windows Vista oder höher.

 

 
