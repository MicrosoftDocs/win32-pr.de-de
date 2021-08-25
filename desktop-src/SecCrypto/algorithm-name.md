---
description: Legt den Algorithmus fest, der zum Signieren, Umgestalten und Verschlüsseln von Vorgängen verwendet wird, oder ruft den Algorithmus ab. Dies ist die Standardeigenschaft.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4d9860e9a3f04f2f17ebcda08a4ec2610c5af3cbb5fbb5e7afa98227264992b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880150"
---
# <a name="algorithmname-property"></a>Algorithm.Name-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Name-Eigenschaft** legt den Algorithmus fest oder ruft den Algorithmus ab, der für Signierungs-, Um- und Verschlüsselungsvorgänge verwendet wird. Dies ist die Standardeigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ ENCRYPTION \_ ALGORITHM-Enumeration,**](capicom-encryption-algorithm.md) der angibt, welcher Algorithmus verwendet werden soll. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                       | Bedeutung                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ RC2**</dt> </dl>    | Verwenden Sie die RC2-Verschlüsselung.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ RC4**</dt> </dl>    | Verwenden Sie die RC4-Verschlüsselung.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ DES**</dt> </dl>    | Verwenden Sie die DES-Verschlüsselung.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ 3DES**</dt> </dl> | Verwenden Sie die Triple DES-Verschlüsselung.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ AES**</dt> </dl>    | Verwenden Sie den AES-Algorithmus.<br/>     |



 

## <a name="remarks"></a>Hinweise

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
