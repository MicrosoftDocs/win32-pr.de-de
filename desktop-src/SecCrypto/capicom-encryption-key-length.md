---
description: Definiert die Schlüssellänge, die bei der Verschlüsselung verwendet werden soll.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: CAPICOM_ENCRYPTION_KEY_LENGTH-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367848"
---
# <a name="capicom_encryption_key_length-enumeration"></a>CAPICOM- \_ Verschlüsselungs \_ Schlüssellänge- \_ Enumeration

Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge** " definiert die [*Schlüssellänge*](../secgloss/k-gly.md) , die bei der Verschlüsselung verwendet werden soll.

## <a name="members"></a>Member



| Member                                          | BESCHREIBUNG                                                                               | Wert     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **\_ \_ \_ \_ maximal zulässige Länge von CAPICOM-Verschlüsselungsschlüsseln**   | Verwendet die maximale Schlüssellänge, die mit dem angegeben Verschlüsselungsalgorithmus verfügbar ist.<br/> | 0         |
| **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 40 \_ Bits**  | Verwendet 40-Bit-Schlüssel.<br/>                                                              | 1         |
| **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 56 \_ Bits**  | Verwendet 56-Bit-Schlüssel, falls verfügbar.<br/>                                                 | 2         |
| **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 128 \_ Bits** | Verwendet 128-Bit-Schlüssel, falls verfügbar.<br/>                                                | 3         |
| **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 192 \_ Bits** | Verwendet 192-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  | 4//v 2.0 |
| **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 256 \_ Bits** | Verwendet 256-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  | 5//v 2.0 |



## <a name="remarks"></a>Bemerkungen

Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge** " wird von der Eigenschaft " [**Algorithmus. keylength**](algorithm-keylength.md) " verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
