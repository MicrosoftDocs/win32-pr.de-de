---
description: Algorithmen können vom Microsoft RSA/SChannel-Kryptografieanbieter unterstützt werden.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: RSA/SChannel-Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359868"
---
# <a name="rsaschannel-provider-algorithms"></a>RSA/SChannel-Anbieter Algorithmen

Die folgenden Algorithmen können vom Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Kryptografieanbieter unterstützt werden.



| Algorithmuskennung    | BESCHREIBUNG                                                                                                                         | Kommentare                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| calg \_ RSA \_ Keyx | RSA-Algorithmus für den [ *Schlüsselaustausch* von öffentlichem Schlüssel](../secgloss/k-gly.md) | Schlüssellänge: kann festgelegt werden, 384 Bits auf 16.384 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 1.024 Bits.<br/> |
| Calg \_ MD5       | MD5-Hashalgorithmus                                                                                                              | Wird nur für hashung bereitgestellt.                                                                                      |
| calg \_ SHA       | SHA-Hashalgorithmus                                                                                                              | Muss für DSS-Signaturen verwendet werden.                                                                                |
| Calg \_ RC2       | RC2-Block Verschlüsselungsalgorithmus.                                                                                                     | Schlüssellänge: 40 bis 88 Bits                                                                                       |
| Calg \_ RC4       | RC4-Stream-Verschlüsselungsalgorithmus.                                                                                                    | Schlüssellänge: 40 bis 88 Bits                                                                                       |



 

 

 
