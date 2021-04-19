---
title: Player. playlistchange-Ereignis
description: Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird. | Player. playlistchange-Ereignis
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player "playlistchange-Ereignisfenster"
- Playlistchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistchange-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360363"
---
# <a name="playerplaylistchange-event"></a>Player. playlistchange-Ereignis

Das **playlistchange** -Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Abspielen* 
</dt> <dd>

**Wiedergabe** Listen Objekt, das geändert wurde.

</dd> <dt>

*change* 
</dt> <dd>

**Zahl** (**Long**), die den Typ der Änderung angibt, die in der Wiedergabeliste aufgetreten ist. Enthält einen der folgenden Werte.



| number | name          |
|--------|---------------|
| 0      | Unbekannt       |
| 1      | Clear         |
| 2      | Infochange    |
| 3      | Move          |
| 4      | Löschen        |
| 5      | Einfügen        |
| 6      | Anfügen        |
| 7      | Nicht unterstützt |
| 8      | Name Change    |
| 9      | Nicht unterstützt |
| 10     | Sortieren          |



 

Die Enumerationskonstante im C-Stil kann durch Voranstellen des Namens Werts mit "wmsps" abgeleitet werden. Beispielsweise ist die Konstante für den Verschiebungs Zustand **wmplcmove**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





