---
description: Definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: CAPICOM_ENCRYPTION_ALGORITHM-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368536"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>CAPICOM- \_ Verschlüsselungs \_ Algorithmus-Enumeration

Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Algorithmus** " definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.

## <a name="members"></a>Member



| Member                                   | BESCHREIBUNG                                                                                                                                                                                              | Wert     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC2**  | Verwenden Sie die RSA RC2-Verschlüsselung.<br/>                                                                                                                                                                       | 0         |
| **CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC4**  | Verwenden Sie die RSA RC4-Verschlüsselung.<br/>                                                                                                                                                                       | 1         |
| **CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ des**  | Verwenden Sie die des-Verschlüsselung.<br/>                                                                                                                                                                           | 2         |
| **CAPICOM \_ \_ -Verschlüsselungsalgorithmus \_ 3DES** | Verwenden Sie die Triple des-Verschlüsselung.<br/>                                                                                                                                                                    | 3         |
| **CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ AES**  | Verwenden Sie den [*Advanced Encryption Standard*](../secgloss/a-gly.md) -Algorithmus (AES). Dieser Wert gilt nur für das Objekt " [**verschlüsselteddata**](encrypteddata.md) ".<br/> | 4//v 2.0 |



## <a name="remarks"></a>Bemerkungen

Der Enumerationstyp des **CAPICOM- \_ Verschlüsselungs \_ Algorithmus** wird von der [**Algorithm.Name**](algorithm-name.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
