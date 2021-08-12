---
title: Player.PlaylistChange-Ereignis
description: Das PlaylistChange-Ereignis tritt auf, wenn sich eine Wiedergabeliste ändert. | Player.PlaylistChange-Ereignis
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- PlaylistChange-Windows Media Player
- PlaylistChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , PlaylistChange-Ereignis
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
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572803"
---
# <a name="playerplaylistchange-event"></a>Player.PlaylistChange-Ereignis

Das **PlaylistChange-Ereignis** tritt auf, wenn sich eine Wiedergabeliste ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* 
</dt> <dd>

**Wiedergabelistenobjekt,** das geändert wurde.

</dd> <dt>

*change* 
</dt> <dd>

**Number** (**long**) gibt den Typ der Änderung an, die an der Wiedergabeliste aufgetreten ist. Enthält einen der folgenden Werte.



| number | name          |
|--------|---------------|
| 0      | Unbekannt       |
| 1      | Löschen         |
| 2      | InfoChange    |
| 3      | Move          |
| 4      | Löschen        |
| 5      | Einfügen        |
| 6      | Anfügen        |
| 7      | Nicht unterstützt |
| 8      | NameChange    |
| 9      | Nicht unterstützt |
| 10     | Sortieren          |



 

Die Enumerationskonst constant im C-Stil kann abgeleitet werden, indem dem Namenswert "wmplc" vorangestellt wird. Die Konstante für den Move-Status ist z. B. **wmplcMove.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





