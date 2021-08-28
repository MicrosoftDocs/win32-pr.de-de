---
title: " include-Direktive"
description: Präprozessordi directive that inserts the contents of the specified file into the source program at the point where the directive appears.
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
ms.openlocfilehash: 079ae2680a2610993c3cd54ac64afdfcbafa25c9
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627466"
---
# <a name="include-directive"></a>\#include-Direktive

Präprozessordi directive that inserts the contents of the specified file into the source program at the point where the directive appears.


| \#include "*dateiname*"       |
|------------------------------|
| \#include <*Dateiname*> |

## <a name="parameters"></a>Parameter

| Element | Beschreibung |
|------|-------------|
| *filename* | Der Dateiname der ein include-Datei, der optional eine Verzeichnisspezifikation vorangestellt ist. Der Dateiname muss eine vorhandene Datei angeben. |

## <a name="remarks"></a>Hinweise

Die \# include-Direktive bewirkt, dass die -Direktive durch den gesamten Inhalt der angegebenen Datei ersetzt wird. Der Präprozessor beendet die Suche, sobald er eine Datei mit dem angegebenen Namen findet. Wenn Sie eine vollständige, eindeutige Pfadspezifikation für die Datei angeben, durchsucht der Präprozessor nur den angegebenen Pfad.

> [!NOTE]
> Das [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) verfügt über einen integrierten Includehandler, der den Schalter /I verwendet. Wenn Sie den Compiler jedoch über die API ausführen, können Sie einen benutzerdefinierten Includehandler bereitstellen, indem Sie die ID3DXInclude-Schnittstelle implementieren.

Der Unterschied zwischen den beiden Syntaxformen ist die Reihenfolge, in der der Präprozessor nach Headerdateien sucht, wenn der Pfad unvollständig angegeben ist, wie in der folgenden Tabelle gezeigt.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Syntaxformat</th>
<th>Präprozessorsuchmuster</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#<b>&quot;</b> <em>Includedateiname</em><b>&quot;</b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>im gleichen Verzeichnis wie die Datei, die die #include enthält.</li>
<li>in den Verzeichnissen aller Dateien, die eine #include-Direktive für die Datei enthalten, die die #include enthält.</li>
<li>in Pfaden, die durch die /I-Compileroption angegeben werden, in der Reihenfolge, in der sie aufgeführt sind.</li>
<li><p>in Pfaden, die von der INCLUDE-Umgebungsvariablen angegeben werden, in der Reihenfolge, in der sie aufgeführt sind.</p>
<blockquote>
[!NOTE]<br />
Die INCLUDE-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert. Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation Ihrer Entwicklungsumgebung.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#<b><</b> <em>Includedateiname</em><b>></b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>in Pfaden, die durch die /I-Compileroption angegeben werden, in der Reihenfolge, in der sie aufgeführt sind.</li>
<li><p>in Pfaden, die von der INCLUDE-Umgebungsvariablen angegeben werden, in der Reihenfolge, in der sie aufgeführt sind.</p>
<blockquote>
[!NOTE]<br />
Die INCLUDE-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert. Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation Ihrer Entwicklungsumgebung.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel ersetzt der Präprozessor die \# include-Direktive durch den Inhalt von stdio.h. Da im Beispiel das Format der eckigen Klammer verwendet wird, sucht der Präprozessor nur in den Verzeichnissen, die von der /I-Compileroption und der INCLUDE-Umgebungsvariablen aufgelistet werden.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Weitere Informationen:

- [Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [ID3D10Include-Schnittstelle](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc)
