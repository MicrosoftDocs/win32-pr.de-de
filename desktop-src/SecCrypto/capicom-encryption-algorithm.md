---
description: Definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: CAPICOM_ENCRYPTION_ALGORITHM -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d0f66c1e8ec59819f4f01c5f46989e1f904930f3699f978b26c6ab7c5107154c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879340"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>CAPICOM \_ ENCRYPTION \_ ALGORITHM-Enumeration

Der **CAPICOM \_ ENCRYPTION \_ ALGORITHM-Enumerationstyp** definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.

## <a name="members"></a>Member



| Member                                   | BESCHREIBUNG                                                                                                                                                                                              | Wert     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **\_CAPICOM-VERSCHLÜSSELUNGSALGORITHMUS \_ \_ RC2**  | Verwenden Sie die RSA RC2-Verschlüsselung.<br/>                                                                                                                                                                       | 0         |
| **\_CAPICOM-VERSCHLÜSSELUNGSALGORITHMUS \_ \_ RC4**  | Verwenden Sie die RSA RC4-Verschlüsselung.<br/>                                                                                                                                                                       | 1         |
| **CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ DES**  | Verwenden Sie die DES-Verschlüsselung.<br/>                                                                                                                                                                           | 2         |
| **CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ 3DES** | Verwenden Sie die dreifache DES-Verschlüsselung.<br/>                                                                                                                                                                    | 3         |
| **AES FÜR \_ CAPICOM-VERSCHLÜSSELUNGSALGORITHMUS \_ \_**  | Verwenden Sie [*Advanced Encryption Standard*](../secgloss/a-gly.md) -Algorithmus (AES). Dieser Wert ist nur für das [**EncryptedData-Objekt**](encrypteddata.md) gültig.<br/> | 4 / v2.0 |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ ENCRYPTION \_ ALGORITHM-Enumerationstyp** wird von der [**Algorithm.Name**](algorithm-name.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
