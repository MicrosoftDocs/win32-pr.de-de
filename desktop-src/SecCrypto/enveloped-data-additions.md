---
description: Listet die Änderungen an den Funktionen für die einumhüllenden Daten auf.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Hinzugefügte Daten Ergänzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348327"
---
# <a name="enveloped-data-additions"></a>Hinzugefügte Daten Ergänzungen

Die folgenden Änderungen wurden an den Funktionen für eingeschlossene Daten vorgenommen:

-   Die Identifizierung des Empfängers kann nicht nur durch Aussteller und Seriennummer (PKCS \# 7 1,5), sondern auch durch einen Schlüssel Bezeichner erfolgen.
-   Es werden drei Empfänger Schlüsselaustausch Optionen bereitgestellt:
    -   Schlüssel Transport mit RSA-Schlüsseln.
    -   Schlüssel Vereinbarung mit Ephemeral-Static Diffie-Hellman algorithmusschlüsseln, die mit 3DES oder RC2 umschließen, oder Ephemeral-Static elliptische Kurve Diffie-Hellman algorithmuschlüsselzeichen, die mit AES umschließt sind
    -   Der Schlüssel Verschlüsselungsschlüssel oder die Schlüssel Übertragung für die e-Mail-Liste, bei dem der Schlüssel zum Verschlüsseln des Inhalts Verschlüsselungsschlüssels bereits an die Empfänger verteilt wurde. RC2, 3DES und AES sind als Schlüssel Wrapping Algorithmen zulässig.
-   Ungeschützte Attribute können in die Nachricht eingeschlossen werden.
-   Ein **originatorinfo** -Feld, das Informationen über den Absender enthält, die Zertifikate und CRLs enthalten können, wurde hinzugefügt.
-   Auf der Grundlage von ECC-Algorithmen (Elliptic Curve Cryptography) und AES ist Windows Vista oder höher erforderlich.

 

 



