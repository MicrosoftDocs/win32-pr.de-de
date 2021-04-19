---
description: Erstellt einen Hash der angegebenen Zeichenfolge.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData. Hash-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359264"
---
# <a name="hasheddatahash-method"></a>HashedData. Hash-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Hash** Methode erstellt einen Hash der angegebenen Zeichenfolge.

## <a name="syntax"></a>Syntax


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Eine Zeichenfolge, die den zu Hashwert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die **Hash** Methode für jedes Datenelement auf. Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der [**value**](hasheddata-value.md) -Eigenschaft verkettet. Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
