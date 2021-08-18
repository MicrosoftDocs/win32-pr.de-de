---
title: ClosedCaption.SAMIFileName
description: Die SAMIFileName-Eigenschaft gibt den Namen der Datei an, die die für die Untertitelung erforderlichen Informationen enthält, oder ruft sie ab.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption.SAMIFileName Windows Media Player
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
ms.openlocfilehash: 22ba314208db3cb5529042011f269f026a4cf2bd4d4b01d1b8d64719b96a5f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119511"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

Die **SAMIFileName-Eigenschaft** gibt den Namen der Datei an, die die für die Untertitelung erforderlichen Informationen enthält, oder ruft diesen ab.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Die SAMI-Datei (Synchronized Accessible Media Interchange) muss die Dateierweiterung SMI oder SAMI verwenden.

Wenn Sie keinen Wert für **SAMIFileName** angeben, ruft diese Eigenschaft eine Zeichenfolge ab, die den Dateinamen oder die URL enthält, die dem aktuellen Medienelement zugeordnet ist. Diese Zuordnung kann auftreten, wenn eine  SAMI-Datei mithilfe des sami-URL-Parameters angegeben wird, oder automatisch, wenn die SAMI-Datei denselben Namen wie der Name der Digitalen Mediendatei hat (mit Ausnahme der Dateierweiterung). Wenn dem aktuellen Medium keine SAMI-Datei zugeordnet ist, ruft diese Eigenschaft eine leere Zeichenfolge ("") ab.

Nachdem Sie einen Wert für **SAMIFileName** angegeben haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert angeben (oder bis ein neues Medienelement mithilfe des *sami* URL-Parameters geöffnet wird). Daher müssen Sie einen neuen Wert für diese Eigenschaft angeben, bevor Sie jedes neue Medienelement wieder geben. Auf diese Weise wird der neue Wert für **SAMIFileName** wirksam, wenn das nächste Medienelement geöffnet wird (oder *wenn Player*.**close** wird aufgerufen. Die Angabe eines neuen Werts **für SAMIFileName** hat keine Auswirkungen auf das aktuelle Medium.

Damit Windows Media Player die SAMI-Datei zurückgibt, die einem bestimmten Medienelement zugeordnet ist, geben Sie einen Wert für **SAMIFileName** an, der einer leeren Zeichenfolge ("") entspricht, bevor Sie das nächste Medienelement wiedergibt.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

In den folgenden JScript Beispielen *wird ClosedCaption verwendet.* **SAMIFileName,** um den Namen einer Untertiteltextdatei anzugeben. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





