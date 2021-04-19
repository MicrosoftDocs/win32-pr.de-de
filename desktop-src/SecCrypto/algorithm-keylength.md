---
description: Legt die Länge des Schlüssels fest oder ruft diese ab.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Algorithmus. keylength-Eigenschaft
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
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369378"
---
# <a name="algorithmkeylength-property"></a>Algorithmus. keylength-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **keylength** -Eigenschaft legt die Länge des Schlüssels fest oder ruft diese ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der-Enumeration der [**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge**](capicom-encryption-key-length.md) , die die Schlüssellänge angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                        | Bedeutung                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_ \_ \_ \_ maximal zulässige Länge von CAPICOM-Verschlüsselungsschlüsseln**</dt> </dl>     | Verwenden Sie die maximale Schlüssellänge, die mit dem angegeben Verschlüsselungsalgorithmus verfügbar ist.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 40 \_ Bits**</dt> </dl>    | Verwenden Sie 40-Bit-Schlüssel.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 56 \_ Bits**</dt> </dl>    | Verwenden Sie bei Verfügbarkeit 56-Bit-Schlüssel.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 128 \_ Bits**</dt> </dl> | Verwenden Sie bei Verfügbarkeit 128-Bit-Schlüssel.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 192 \_ Bits**</dt> </dl> | Verwenden Sie 192-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 256 \_ Bits**</dt> </dl> | Verwenden Sie 256-Bit-Schlüssel. Diese Schlüssellänge ist nur für AES verfügbar.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn der-und 3DES-Verschlüsselungsalgorithmen verwendet werden, sind die Schlüssellängen Standard, und die **keylength** -Eigenschaft wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Algorithmus**](algorithm.md)
</dt> </dl>

 

 
