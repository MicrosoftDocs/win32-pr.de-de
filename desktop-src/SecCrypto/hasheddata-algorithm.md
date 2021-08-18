---
description: Legt den Typ des verwendeten Hashalgorithmus fest oder ruft sie ab.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData.Algorithm-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16562f3b954c9968899b7af63729a105956c7f809d094bdfa6c508a160a6d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006648"
---
# <a name="hasheddataalgorithm-property"></a>HashedData.Algorithm-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Algorithm-Eigenschaft** legt den Typ des verwendeten Hashalgorithmus fest oder ruft sie ab.

## <a name="syntax"></a>Syntax


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ HASH \_ ALGORITHM-Enumeration,**](capicom-hash-algorithm.md) der einen Hashalgorithmus definiert. Der Standardwert ist CAPICOM \_ HASH \_ ALGORITHM \_ SHA1. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                               | Bedeutung                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**CAPICOM \_ HASH \_ ALGORITHM \_ SHA1**</dt> </dl>           | SHA1-Hashalgorithmus.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**CAPICOM \_ HASH \_ ALGORITHM \_ MD2**</dt> </dl>              | MD2-Hashalgorithmus<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**CAPICOM \_ HASH \_ ALGORITHM \_ MD4**</dt> </dl>              | MD4-Hashalgorithmus<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**CAPICOM \_ HASH \_ ALGORITHM \_ MD5**</dt> </dl>              | MD5-Hashalgorithmus<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**CAPICOM \_ HASH ALGORITHM SHA \_ \_ \_ 256**</dt> </dl> | SHA-256-Hashalgorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**CAPICOM \_ HASH ALGORITHM SHA \_ \_ \_ 384**</dt> </dl> | SHA-384-Hashalgorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**CAPICOM \_ HASH ALGORITHM SHA \_ \_ \_ 512**</dt> </dl> | SHA-512-Hashalgorithmus.<br/> **CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
