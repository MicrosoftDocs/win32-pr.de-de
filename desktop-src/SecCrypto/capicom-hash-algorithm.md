---
description: Die CAPICOM- \_ Hash \_ Algorithmus-Enumeration definiert einen Hash Algorithmus.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: CAPICOM_HASH_ALGORITHM-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368413"
---
# <a name="capicom_hash_algorithm-enumeration"></a>CAPICOM- \_ Hash \_ Algorithmus-Enumeration

Die **CAPICOM- \_ Hash \_ Algorithmus** -Enumeration definiert einen Hash Algorithmus.

## <a name="members"></a>Member



| Member                                 | BESCHREIBUNG                                                                                                                                                                 | Wert |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM- \_ Hash \_ Algorithmus \_ SHA1**     | [*Secure Hash-Algorithmus*](../secgloss/s-gly.md) (SHA), der einen 160-Bit-Nachrichten Digest generiert.<br/> | 0     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ MD2**      | MD2-Hashalgorithmus<br/>                                                                                                                                           | 1     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ MD4**      | MD4-Hashalgorithmus<br/>                                                                                                                                           | 2     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ MD5**      | MD5-Hashalgorithmus<br/>                                                                                                                                           | 3     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 256** | SHA-256-Hash Algorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/>                                                                 | 4     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 384** | SHA-384-Hash Algorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/>                                                                 | 5     |
| **CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 512** | SHA-512-Hash Algorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/>                                                                 | 6     |



## <a name="remarks"></a>Bemerkungen

Die **CAPICOM- \_ Hash \_ Algorithmus** -Enumeration wird von der [**hashedData. algorithmuseigenschaft**](hasheddata-algorithm.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
