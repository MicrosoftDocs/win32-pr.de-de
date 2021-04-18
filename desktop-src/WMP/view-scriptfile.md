---
title: Scriptfile anzeigen
description: Das scriptfile-Attribut gibt die Dateinamen der begleitenden JScript-Dateien an.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- View. scriptfile-Windows-Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371672"
---
# <a name="viewscriptfile"></a>Scriptfile anzeigen

Das **scriptfile** -Attribut gibt die Dateinamen der begleitenden JScript-Dateien an.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Mögliche Werte

Bei diesem Attribut handelt es sich um eine schreibgeschützte **Zeichenfolge** ohne Standardwert. Die Dateinamen mehrerer JScript-Dateien werden durch Semikolons getrennt. Führende und folgende Leerzeichen und Semikolons sollten nicht vorhanden sein.

## <a name="remarks"></a>Bemerkungen

Der Code in den angegebenen Dateien kann von jedem Ereignishandler in der Ansicht verwendet werden. Code, der von Ereignis Handlern in mehreren Ansichten verwendet wird, kann in einer Datei mit dem gleichen Namen wie die Skin-Definitionsdatei, jedoch mit der Erweiterung. js anstelle der Erweiterung. WMS abgelegt werden. Diese Datei wird automatisch geladen und muss nicht in der Skin-Definitionsdatei angegeben werden.

## <a name="examples"></a>Beispiele


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> </dl>

 

 





