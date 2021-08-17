---
description: Legt die Länge des Schlüssels fest oder ruft sie ab.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Algorithm.KeyLength-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c5ce8f906628df06ef506a0f57c33db4bed7c5980bb78ab2e0094d0443b5646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773664"
---
# <a name="algorithmkeylength-property"></a>Algorithm.KeyLength-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**Namespace System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **KeyLength-Eigenschaft** legt die Länge des Schlüssels fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH-Enumeration,**](capicom-encryption-key-length.md) der die Schlüssellänge angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                        | Bedeutung                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**MAXIMALE LÄNGE DES \_ CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELS \_ \_ \_**</dt> </dl>     | Verwenden Sie die maximale Verfügbare Schlüssellänge mit dem angegebenen Verschlüsselungsalgorithmus.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 40 \_ BITS**</dt> </dl>    | Verwenden Sie 40-Bit-Schlüssel.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 56 \_ BITS**</dt> </dl>    | Verwenden Sie 56-Bit-Schlüssel, falls verfügbar.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**\_CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELLÄNGE \_ \_ \_ 128 \_ BITS**</dt> </dl> | Verwenden Sie 128-Bit-Schlüssel, falls verfügbar.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH \_ 192 \_ BITS**</dt> </dl> | Verwenden Sie 192-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**\_CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELLÄNGE \_ \_ \_ 256 \_ BITS**</dt> </dl> | Verwenden Sie 256-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Wenn DES- und 3DES-Verschlüsselungsalgorithmen verwendet werden, sind die Schlüssellängen Standard, und die **KeyLength-Eigenschaft** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Algorithmus**](algorithm.md)
</dt> </dl>

 

 
