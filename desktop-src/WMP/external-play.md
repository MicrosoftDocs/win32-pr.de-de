---
title: Extern. Play-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Play-Methode weist Windows Media Player an, einen Satz von Medien Elementen wiederzugeben.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Wiedergabemethode Windows Media Player
- Wiedergabemethode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Wiedergabemethode
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
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355886"
---
# <a name="externalplay-method"></a>Extern. Play-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **Play** -Methode weist Windows Media Player an, einen Satz von Medien Elementen wiederzugeben.

## <a name="syntax"></a>Syntax


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Librarylocationtype* \[ in\]
</dt> <dd>

Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der zu Wiedergabe enden Medienelemente angibt. Cpalbumid gibt beispielsweise an, dass ein oder mehrere Alben wiedergegeben werden sollen.

</dd> <dt>

*Librarylocationids* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** mit den Bezeichnerzeichen, die durch Semikolons getrennt sind, der zu Wiedergabe enden Medienelemente.

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

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





