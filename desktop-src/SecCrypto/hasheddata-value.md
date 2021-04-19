---
description: Ruft die Hash Daten nach erfolgreichen Aufrufen der Hash Methode ab.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData. Value (Eigenschaft)
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
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373652"
---
# <a name="hasheddatavalue-property"></a>HashedData. Value (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **value** -Eigenschaft ruft die Hash Daten nach erfolgreichen Aufrufen der [**Hash**](hasheddata-hash.md) Methode ab. Der Hashwert wird im Hexadezimal Format zurückgegeben. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Hash Daten im Hexadezimal Format enthält.

## <a name="remarks"></a>Bemerkungen

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hash**](hasheddata-hash.md) Methode für jedes Datenelement auf. Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der **value** -Eigenschaft verkettet. Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
