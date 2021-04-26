---
description: Platziert eine C- oder IDL-Include-Anweisung im generierten Code.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995127"
---
# <a name="literalinclude-element"></a>literalInclude-Element

Platziert eine C- oder IDL-Include-Anweisung im generierten Code.

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
<td>Sprachzeichenfolge<br/></td>
<td>Nein<br/></td>
<td>Der Typ der header-Datei, die eingeschlossen werden soll. <br/> <br/>
<dt><strong>C</strong></dt> <dd> Schließen Sie eine C-Headerdatei ein.<br/> </dd> <dt><strong>Idl</strong></dt> <dd> Schließen Sie eine IDL-Datei ein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Lokal</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Dieses Attribut wird nur verwendet, wenn <strong>Language</strong> auf C festgelegt &quot; &quot; ist.<br/> <br/>
<dt><strong>STIMMT</strong></dt> <dd> Durchsucht das aktuelle Verzeichnis nach dem benannten Header, bevor die Systemverzeichnisse durchsucht werden.<br/> </dd> <dt><strong>FALSE</strong></dt> <dd> Durchsuchen Sie nur Systemverzeichnisse nach dem benannten Header.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die folgenden Beispiele zeigen den Code, der aus verschiedenen **literalInclude-Elementen** generiert wurde.

### <a name="example-1---generating-a-c-include-statement"></a>Beispiel 1: Generieren einer C-Include-Anweisung

Eingabe-XML:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Ausgabecode:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Beispiel 2: Generieren einer Include-Anweisung in C

Eingabe-XML:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Ausgabecode:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Beispiel 3: Generieren einer IDL-Import-Anweisung

Eingabe-XML:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Ausgabecode:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




