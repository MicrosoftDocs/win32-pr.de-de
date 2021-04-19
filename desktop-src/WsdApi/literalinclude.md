---
description: Fügt eine C-oder IDL-include-Anweisung in den generierten Code ein.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalinclude-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356206"
---
# <a name="literalinclude-element"></a>literalinclude-Element

Fügt eine C-oder IDL-include-Anweisung in den generierten Code ein.

## <a name="usage"></a>Verbrauch

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Sprache</strong><br/></td>
<td>sprach Zeichenfolge<br/></td>
<td>Nein<br/></td>
<td>Der Typ der Header Datei, die eingeschlossen werden soll. <br/> <br/>
<dt><strong>Scher</strong></dt> <dd> Fügen Sie eine C-Header Datei ein.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Fügen Sie eine IDL-Datei ein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Lokal</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Dieses Attribut wird nur verwendet, wenn <strong>Language</strong> auf C festgelegt ist &quot; &quot; .<br/> <br/>
<dt><strong>Fall</strong></dt> <dd> Durchsucht das aktuelle Verzeichnis nach dem benannten Header, bevor die Systemverzeichnisse durchsucht werden.<br/> </dd> <dt><strong>Alarm</strong></dt> <dd> Systemverzeichnisse werden nur nach dem benannten Header durchsucht.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

In den folgenden Beispielen wird der Code gezeigt, der aus verschiedenen **literalinclude** -Elementen generiert wurde.

### <a name="example-1---generating-a-c-include-statement"></a>Beispiel 1: Erstellen einer C include-Anweisung

Eingabe-XML:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Ausgabe Code:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Beispiel 2: Erstellen einer C include-Anweisung

Eingabe-XML:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Ausgabe Code:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Beispiel 3: Erstellen einer IDL-Import Anweisung

Eingabe-XML:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Ausgabe Code:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




