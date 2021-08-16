---
description: Definiert die Schlüssellänge, die bei der Verschlüsselung verwendet werden soll.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: CAPICOM_ENCRYPTION_KEY_LENGTH -Enumeration (Capicom.h)
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
ms.openlocfilehash: 2957bd644fdf405fec7e82a487bf83af2cbae35ae305f10b9b168628a30b0749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772475"
---
# <a name="capicom_encryption_key_length-enumeration"></a>CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH-Enumeration

Der **ENUMERATIONstyp CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH** definiert die [*Schlüssellänge,*](../secgloss/k-gly.md) die bei der Verschlüsselung verwendet werden soll.

## <a name="members"></a>Member



| Member                                          | Beschreibung                                                                               | Wert     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **MAXIMALE LÄNGE DES \_ CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELS \_ \_ \_**   | Verwendet die maximale Verfügbare Schlüssellänge mit dem angegebenen Verschlüsselungsalgorithmus.<br/> | 0         |
| **CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 40 \_ BITS**  | Verwendet 40-Bit-Schlüssel.<br/>                                                              | 1         |
| **CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 56 \_ BITS**  | Verwendet 56-Bit-Schlüssel, falls verfügbar.<br/>                                                 | 2         |
| **\_CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELLÄNGE \_ \_ \_ 128 \_ BITS** | Verwendet 128-Bit-Schlüssel, falls verfügbar.<br/>                                                | 3         |
| **CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 192 \_ BITS** | Verwendet 192-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  | 4 / v2.0 |
| **\_CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELLÄNGE \_ \_ \_ 256 \_ BITS** | Verwendet 256-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  | 5 / v2.0 |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ ENCRYPTION KEY \_ LENGTH-Enumerationstyp \_** wird von der [**Algorithm.KeyLength-Eigenschaft**](algorithm-keylength.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
