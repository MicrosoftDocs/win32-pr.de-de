---
title: " include-Direktive"
description: Eine Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quell Programm einfügt, wenn die Anweisung angezeigt wird.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include-Direktive HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993438"
---
# <a name="include-directive"></a>\#include-Direktive

Eine Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quell Programm einfügt, wenn die Anweisung angezeigt wird.


| \#"*Dateiname*" einschließen       |
|------------------------------|
| \#<*Dateiname* einschließen> |

## <a name="parameters"></a>Parameter

| Element | Beschreibung |
|------|-------------|
| *filename* | Der Dateiname der einzuschließenden Datei, dem optional eine Verzeichnis Spezifikation vorangestellt. Der Dateiname muss eine vorhandene Datei angeben. |

## <a name="remarks"></a>Bemerkungen

Die \# include-Direktive bewirkt, dass die-Direktive durch den gesamten Inhalt der angegebenen Datei ersetzt wird. Der Präprozessor beendet die Suche, sobald eine Datei mit dem angegebenen Namen gefunden wird. Wenn Sie eine eindeutige Pfadspezifikation für die Datei angeben, durchsucht der Präprozessor nur den angegebenen Pfad.

> [!NOTE]
> Das [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) verfügt über einen integrierten include-Handler, der den/I-Schalter verwendet. Wenn Sie jedoch den Compiler über die API ausführen, können Sie einen benutzerdefinierten include-Handler bereitstellen, indem Sie die ID3DXInclude-Schnittstelle implementieren.

Der Unterschied zwischen den beiden Syntax Formularen ist die Reihenfolge, in der der Präprozessor nach Header Dateien sucht, wenn der Pfad nicht vollständig angegeben ist, wie in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Syntaxformat</th>
<th>Präprozessorsuchmuster</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#<b>&quot;</b> <em>Dateiname</em> einschließen<b>&quot;</b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>im gleichen Verzeichnis wie die Datei, die die #include-Direktive enthält.</li>
<li>in den Verzeichnissen von Dateien, die eine #include-Direktive für die Datei enthalten, die die #include-Direktive enthält.</li>
<li>in der von der/I-Compileroption angegebenen Pfade in der Reihenfolge, in der Sie aufgelistet sind.</li>
<li><p>in den Pfaden, die durch die include-Umgebungsvariable angegeben werden, in der Reihenfolge, in der Sie aufgelistet sind.</p>
<blockquote>
[!NOTE]<br />
Die include-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert. Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation der Entwicklungsumgebung.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#<b><</b> <em>Dateiname</em> einschließen<b>></b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>in der von der/I-Compileroption angegebenen Pfade in der Reihenfolge, in der Sie aufgelistet sind.</li>
<li><p>in den Pfaden, die durch die include-Umgebungsvariable angegeben werden, in der Reihenfolge, in der Sie aufgelistet sind.</p>
<blockquote>
[!NOTE]<br />
Die include-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert. Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation der Entwicklungsumgebung.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Beispiele

Das folgende Beispiel bewirkt, dass der Präprozessor die \# include-Direktive durch den Inhalt von "stdio. h" ersetzt. Da im Beispiel das eckige Klammern-Format verwendet wird, sucht der Präprozessor nur in den Verzeichnissen, die von der/I-Compileroption und der INCLUDE-Umgebungsvariablen aufgelistet werden.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Weitere Informationen

- [Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [ID3D10Include-Schnittstelle](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc)