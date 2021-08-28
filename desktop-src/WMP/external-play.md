---
title: External.play-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die Play-Methode weist Windows Media Player, einen Satz von Medienelementen wieder zu spielen.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Play-Windows Media Player
- play method Windows Media Player , External class
- Externe Klasse Windows Media Player , Play-Methode
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90644b357e56f40bfbdb576908b99aa6941f8153dc339daa996152f63d77372c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648630"
---
# <a name="externalplay-method"></a>External.play-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **Play-Methode** weist Windows Media Player, einen Satz von Medienelementen wieder zu spielen.

## <a name="syntax"></a>Syntax


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LibraryLocationType* \[ In\]
</dt> <dd>

Eine [Bibliotheksspeicherort-Konstante,](library-location-constants.md) die den Typ der Medienelemente angibt, die abgespielt werden sollen. Beispielsweise gibt CP CpuID an, dass ein oder mehrere Albums abgespielt werden sollen.

</dd> <dt>

*LibraryLocationIDs* \[ In\]
</dt> <dd>

**Eine** Zeichenfolge, die die durch Semikolons getrennten Bezeichner der medienelemente enthält, die abgespielt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





