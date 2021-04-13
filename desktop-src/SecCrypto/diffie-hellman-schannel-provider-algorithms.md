---
description: Der Zweck des Diffie-Hellman Algorithmus besteht darin, dass zwei oder mehr Hosts einen identischen geheimen Verschlüsselungsschlüssel erstellen und freigeben können, indem Sie einfach Informationen über ein Netzwerk freigeben, das nicht sicher ist.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Diffie-Hellman/SChannel-Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350139"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Diffie-Hellman/SChannel-Anbieter Algorithmen

Der Zweck des Diffie-Hellman Algorithmus besteht darin, dass zwei oder mehr Hosts einen identischen geheimen Verschlüsselungsschlüssel erstellen und freigeben können, indem Sie einfach Informationen über ein Netzwerk freigeben, das nicht sicher ist. Die Informationen, die über das Netzwerk freigegeben werden, sind in Form von einigen Konstanten Werten und einem öffentlichen D-H-Schlüssel.

Der Kryptografieanbieter Microsoft [*Diffie-Hellman*](../secgloss/d-gly.md) / [*SChannel*](../secgloss/s-gly.md) unterstützt die folgenden Algorithmen.



| Algorithmuskennung                  | BESCHREIBUNG                                                                                                                                           | Kommentare                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| "calg \_ dh \_ SF"                  | Diffie-Hellman zum Speichern und Weiterleiten des [ *Schlüsselaustausch Algorithmus*](../secgloss/k-gly.md) | Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 512 Bits.<br/> |
| Calg \_ MD5                     | MD5-Hashalgorithmus                                                                                                                                | Wird nur für hashung bereitgestellt.                                                                                 |
| calg \_ dh- \_ ephem               | Kurzlebiger D-H-Schlüsselaustausch.                                                                                                                           | Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 512 Bits.<br/> |
| calg \_ SHA                     | SHA-Hashalgorithmus                                                                                                                                | Muss für DSS-Signaturen verwendet werden.                                                                           |
| Calg \_ RC2                     | RC2-Block Verschlüsselungsalgorithmus                                                                                                                        | Schlüssellänge: 40 bis 88 Bits.                                                                                 |
| Calg \_ RC4                     | RC4-Stream-Verschlüsselungsalgorithmus                                                                                                                       | Schlüssellänge: 40 bis 88 Bits.                                                                                 |
| calg \_ Cylink \_ MEK<br/> | DES Variant-Verschlüsselungsalgorithmus                                                                                                                      | Schlüssellänge: 40 Bits.                                                                                       |



 

 

 
