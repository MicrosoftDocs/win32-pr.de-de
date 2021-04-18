---
title: Closedcaption. samifilename
description: Die samifilename-Eigenschaft gibt den Namen der Datei an, die die für den Untertitel erforderlichen Informationen enthält, oder ruft ihn ab.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Closedcaption. samifilename-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364896"
---
# <a name="closedcaptionsamifilename"></a>Closedcaption. samifilename

Die **samifilename** -Eigenschaft gibt den Namen der Datei an, die die für den Untertitel erforderlichen Informationen enthält, oder ruft ihn ab.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die in der Synchronisierung verfügbare Medienaustausch Datei (Sami) muss eine SMI-oder. Sami-Dateinamenerweiterung verwenden.

Wenn Sie keinen Wert für **samifilename** angeben, ruft diese Eigenschaft eine Zeichenfolge ab, die den Dateinamen oder die URL enthält, die dem aktuellen Medien Element zugeordnet ist. Diese Zuordnung kann auftreten, wenn eine Sami-Datei mithilfe des *Sami* URL-Parameters angegeben wird, oder automatisch, wenn die Sami-Datei den gleichen Namen hat wie der Name der digitalen Mediendatei (mit Ausnahme der Dateinamenerweiterung). Wenn dem aktuellen Medium keine samische Datei zugeordnet ist, ruft diese Eigenschaft eine leere Zeichenfolge ("") ab.

Nachdem Sie einen Wert für **samifilename** angegeben haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert angeben (oder bis ein neues Medien Element mithilfe des *Sami* URL-Parameters geöffnet wird). Daher müssen Sie einen neuen Wert für diese Eigenschaft angeben, bevor Sie die einzelnen neuen Medienelemente wiedergeben. Auf diese Weise wird der neue Wert für **samifilename** wirksam, wenn das nächste Medien Element geöffnet wird (oder wenn *Player*.**Close** wird aufgerufen.) Das Angeben eines neuen Werts für **samifilename** hat keine Auswirkung auf das aktuelle Medium.

Um zu bewirken, dass Windows Media Player die mit einem bestimmten Medien Element verknüpfte Sami-Datei zurückgibt, geben Sie einen Wert für **samifilename** an, der einer leeren Zeichenfolge ("") entspricht, bevor Sie das nächste Medien Element wiedergeben.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

In den folgenden drei JScript-Beispielen wird *closedcaption* verwendet. **Samifilename** zum Angeben des Namens einer Textdatei mit geschlossener Beschriftung. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





