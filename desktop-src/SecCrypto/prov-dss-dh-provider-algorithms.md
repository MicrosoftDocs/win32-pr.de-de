---
description: Von Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter unterstützte Algorithmen.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: PROV_DSS_DH Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366494"
---
# <a name="prov_dss_dh-provider-algorithms"></a>Prov- \_ DSS- \_ dh-Anbieter Algorithmen

In der folgenden Tabelle werden die Algorithmen aufgelistet, die vom Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter unterstützt werden.



| Algorithmuskennung      | BESCHREIBUNG                                 | Kommentare                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Calg \_ MD5         | MD5-Hashalgorithmus                      | Wird nur für hashung bereitgestellt.                                                                                      |
| calg \_ SHA         | SHA-Hashalgorithmus                      | Muss für DSS-Signaturen verwendet werden.                                                                                |
| Calg \_ SHA1        | Identisch mit calg \_ SHA.                          | Kein Kommentar.                                                                                                     |
| calg- \_ DSS- \_ Zeichen   | DSS-Algorithmus für die öffentliche/private Schlüssel Signatur. | Schlüssellänge: kann festgelegt werden, 512 Bits auf 1.024 Bits in 64-Bit-Inkrementen. Standard Schlüssellänge: 1.024 Bits.<br/> |
| "calg \_ dh \_ SF"      | Speichern und Weiterleiten von D-H-Schlüsselaustausch.         | Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 512 Bits.<br/>      |
| calg \_ dh- \_ ephem   | Kurzlebiger D-H-Schlüsselaustausch.                 | Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 512 Bits.<br/>      |
| calg \_ Cylink \_ MEK | Eine 40-Bit-Variante eines des-Schlüssels.              | Schlüssellänge: 40 Bits.                                                                                            |



 

 

 




