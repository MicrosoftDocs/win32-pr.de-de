---
description: Das folgende Material ist nur gültig, wenn Digest als SASL-Mechanismus verwendet wird. Chiffren und Verschlüsselung sind nicht für die HTTP-Authentifizierung mit Microsoft Digest verfügbar.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215359"
---
# <a name="ciphers"></a>Ciphers

Das folgende Material ist nur gültig, wenn Digest als SASL-Mechanismus verwendet wird. Chiffren und Verschlüsselung sind nicht für die HTTP-Authentifizierung mit Microsoft Digest verfügbar.

Die Chiffre Direktive der Digest SASL Challenge enthält eine Liste der Chiffren, die von einem Server unterstützt werden, für den vertrauliche Kommunikation erforderlich ist. Die Chiffre Direktive kann nur eingeschlossen werden, wenn die QoP-Direktive auf "auth-conf" festgelegt ist. Die Chiffren, die von Microsoft Digest erkannt werden, sind in der folgenden Tabelle aufgeführt, von der stärksten zum schwächsten.



| Chiffre Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RC4        | Die RC4-Chiffre mit einem 128-Bit-Schlüssel.                                                                                                                                                                                                                                                             |
| 3DES       | Das [*dreifache*](/windows/desktop/SecGloss/t-gly) der-Verschlüsselung im [*CBC*](/windows/desktop/SecGloss/c-gly) -Modus mit "Ede" mit dem gleichen Schlüssel für jede E-Phase (zwei Schlüssel Modus). Die Gesamtlänge des Schlüssels beträgt 112 Bits. |
| "RC4-56"     | Die RC4-Chiffre mit einem 56-Bit-Schlüssel.                                                                                                                                                                                                                                                              |
| "RC4-40"     | Die RC4-Chiffre mit einem 40-Bit-Schlüssel.                                                                                                                                                                                                                                                              |
| des        | Der [*Verschlüsselungs Standard (Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) , des) in [*Verschlüsselungs Block Verkettung*](/windows/desktop/SecGloss/c-gly) (CBC)-Modus mit einem 56-Bit-Schlüssel. |



 

Wenn eine Serveranwendung Vertraulichkeit (QoP = "auth-conf") anfordert Microsoft Digest generiert eine Herausforderung, die dem Client alle auf dem Server installierten Chiffren bietet und von Digest unterstützt wird. Der digestclient wählt die stärkste verfügbare Chiffre aus. Ausführliche Informationen zum Angeben der Vertraulichkeit finden Sie unter [Erstellen der Digest-Challenge](generating-the-digest-challenge.md).

 

 
