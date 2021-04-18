---
title: Wiedergabeliste. setcolumnresizemode
description: Die setcolumnresizemode-Methode gibt die Größe der indizierten Spalten an.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Wiedergabeliste. setcolumnresizemode (Windows Media Player)
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372770"
---
# <a name="playlistsetcolumnresizemode"></a>Wiedergabeliste. setcolumnresizemode

Die **setcolumnresizemode** -Methode gibt die Größe der indizierten Spalten an.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Kolumne*
</dt> <dd>

**Zahl** (**Long**), die den Index der zu ändernden Spalte angibt.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Spar*
</dt> <dd>

**Zeichenfolge** , die den Größen Anpassungsmodus angibt. Enthält einen der folgenden Werte.



| Wert          | BESCHREIBUNG                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| Autosizeheader | Die Größe der Spaltengröße wird an alle Daten in der Spalte und in der Kopfzeile angepasst.                                  |
| Autosizedata   | Die Spaltengröße ändert sich, um nur alle Daten in der Spalte zu unterstützen.                                                 |
| Fest          | Die Spalte hat eine Größe mit fester Größe.                                                                                    |
| Dehn      | Die Größe der Spalte ändert sich, um den verbleibenden Platz im **Wiedergabe** Listenelement zu verwenden, nachdem alle anderen Spalten geändert wurden. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> </dl>

 

 





