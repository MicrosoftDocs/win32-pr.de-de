---
description: Ruft die Hashdaten nach erfolgreichen Aufrufen der Hash-Methode ab.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData.Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a6b8b2c8291e793cd88c5d4b0821c036fb6b112beb87e73d4f8ccb8d523deb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006568"
---
# <a name="hasheddatavalue-property"></a>HashedData.Value-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Value-Eigenschaft** ruft die Hashdaten nach erfolgreichen Aufrufen der [**Hashmethode**](hasheddata-hash.md) ab. Der Hashwert wird im Hexadezimalformat zurückgegeben. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Hashdaten im Hexadezimalformat enthält.

## <a name="remarks"></a>Hinweise

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hash-Methode**](hasheddata-hash.md) für jedes Datenstück auf. Der Hash jedes Datenstücks wird mit der **Value-Eigenschaft** verkettet, bis die Eigenschaft gelesen wird. Der Inhalt der **Value-Eigenschaft** wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

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

 

 
