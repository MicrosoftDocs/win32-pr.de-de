---
title: VIEW.scriptFile
description: Das scriptFile-Attribut gibt die Dateinamen der zugehörigen JScript Dateien an.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- VIEW.scriptFile-Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f22b0fb5f0815c8977a363c033d26c0d68f725e0cdcd546bc2f2c1a7b723c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615330"
---
# <a name="viewscriptfile"></a>VIEW.scriptFile

Das **scriptFile-Attribut** gibt die Dateinamen der zugehörigen JScript Dateien an.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **zeichenfolge** ohne Schreibzugriff ohne Standardwert. Die Dateinamen mehrerer JScript Dateien sind durch Semikolons getrennt. Führende und folgende Leerzeichen und Semikolons dürfen nicht vorhanden sein.

## <a name="remarks"></a>Hinweise

Der Code in den angegebenen Dateien kann von jedem Ereignishandler in der Ansicht verwendet werden. Code, der von Ereignishandlern in mehreren Ansichten verwendet wird, kann in einer Datei mit dem gleichen Namen wie die Skindefinitionsdatei platziert werden, jedoch mit einer .js Erweiterung anstelle einer WMS-Erweiterung. Diese Datei wird automatisch geladen und muss nicht in der Skindefinitionsdatei angegeben werden.

## <a name="examples"></a>Beispiele


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> </dl>

 

 





