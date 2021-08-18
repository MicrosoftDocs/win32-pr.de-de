---
description: Erstellt einen Hash der angegebenen Zeichenfolge.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData.Hash-Methode
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
ms.openlocfilehash: 2828f54f754591d1b0027a6c892dc57e8b5cdfecc5e9759985b74b1dffef9fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006578"
---
# <a name="hasheddatahash-method"></a>HashedData.Hash-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Hash-Methode** erstellt einen Hash der angegebenen Zeichenfolge.

## <a name="syntax"></a>Syntax


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

Eine Zeichenfolge, die den zu hashenden Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die **Hash-Methode** für jedes Datenstück auf. Der Hash der einzelnen Daten wird mit der [**Value-Eigenschaft**](hasheddata-value.md) verkettet, bis die Eigenschaft gelesen wird. Der Inhalt der **Value-Eigenschaft** wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
