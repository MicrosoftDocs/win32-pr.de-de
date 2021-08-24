---
title: " include-Direktive"
description: Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quellprogramm an dem Punkt einfügt, an dem die Direktive angezeigt wird.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include-Anweisung HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66df429785a9fb90d2de8c89d23792c1754e2fde8eeb4770912e65a41a622c3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855040"
---
# <a name="include-directive"></a>\#include-Direktive

Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quellprogramm an dem Punkt einfügt, an dem die Direktive angezeigt wird.


| \#include "*filename*"       |
|------------------------------|
| \#include <*Filename*> |

## <a name="parameters"></a>Parameter

| Element | Beschreibung |
|------|-------------|
| *filename* | Der Dateiname der einzufügenden Datei, optional vorangestellt durch eine Verzeichnisspezifikation. Der Dateiname muss eine vorhandene Datei angeben. |

## <a name="remarks"></a>Hinweise

Die \# include-Direktive bewirkt, dass die -Direktive durch den gesamten Inhalt der angegebenen Datei ersetzt wird. Der Präprozessor beendet die Suche, sobald er eine Datei mit dem angegebenen Namen findet. Wenn Sie eine vollständige, eindeutige Pfadspezifikation für die Datei angeben, durchsucht der Präprozessor nur den angegebenen Pfad.

> [!NOTE]
> Das [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) verfügt über einen integrierten Includehandler, der den Schalter /I verwendet. Beim Ausführen des Compilers über die API können Sie jedoch einen benutzerdefinierten Includehandler bereitstellen, indem Sie die ID3DXInclude-Schnittstelle implementieren.

Der Unterschied zwischen den beiden Syntaxformen ist die Reihenfolge, in der der Präprozessor nach Headerdateien sucht, wenn der Pfad unvollständig angegeben ist, wie in der folgenden Tabelle dargestellt.

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
<td>#include <b>&quot;</b> <em>filename</em><b>&quot;</b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>im gleichen Verzeichnis wie die Datei, die die #include-Direktive enthält.</li>
<li>in den Verzeichnissen aller Dateien, die eine #include-Direktive für die Datei enthalten, die die #include-Direktive enthält.</li>
<li>in Pfaden, die von der Compileroption /I angegeben werden, in der Reihenfolge, in der sie aufgelistet werden.</li>
<li><p>in Pfaden, die von der INCLUDE-Umgebungsvariablen angegeben werden, in der Reihenfolge, in der sie aufgelistet werden.</p>
<blockquote>
[!NOTE]<br />
Die INCLUDE-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert. Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation Ihrer Entwicklungsumgebung.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#include <b><</b> <em>filename</em><b>></b></td>
<td>Sucht nach der Includedatei:
<ol>
<li>in Pfaden, die von der Compileroption /I angegeben werden, in der Reihenfolge, in der sie aufgelistet werden.</li>
<li><p>in Pfaden, die von der INCLUDE-Umgebungsvariablen angegeben werden, in der Reihenfolge, in der sie aufgelistet werden.</p>
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

Das folgende Beispiel bewirkt, dass der Präprozessor die \# include-Direktive durch den Inhalt von stdio.h ersetzt. Da im Beispiel das Format der spitzen Klammern verwendet wird, sucht der Präprozessor nur in den Verzeichnissen, die von der /I-Compileroption und der INCLUDE-Umgebungsvariablen aufgelistet werden, nach der Datei.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Weitere Informationen

- [Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [ID3D10Include-Schnittstelle](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Effektcompilertool](/windows/desktop/direct3dtools/fxc)