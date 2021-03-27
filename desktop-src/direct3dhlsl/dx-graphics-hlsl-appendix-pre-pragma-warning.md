---
title: warning-pragma-Direktive
description: Pragma-Direktive, die das Verhalten von compilerwarnungs Meldungen ändert.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- warning-pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948198"
---
# <a name="warning-pragma-directive"></a>warning-pragma-Direktive

Pragma-Direktive, die das Verhalten von compilerwarnungs Meldungen ändert.



| \#pragma-Warnung ( *Warning-specifier* : *Warning-Number-List* \[ ; *Warning-specifier* : *Warning-Number-List*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warnungsspezifizierer</em><br/></td>
<td>Das für die angegebenen Warnungen festzulegende Verhalten. Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen. <br/> 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>Zeigt die Meldung der Warnungen mit den angegebenen Zahlen nur einmal an.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Setzt das Verhalten der Warnungen mit den angegebenen Zahlen auf ihren Standardwert zurück. Dies hat auch den Effekt, dass eine Warnung aktiviert wird, die standardmäßig deaktiviert ist. Die Warnung wird auf der Standard Ebene generiert.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Wendet die angegebene Ebene auf die Warnungen mit den angegebenen Zahlen an. Dies hat auch den Effekt, dass eine Warnung aktiviert wird, die standardmäßig deaktiviert ist.</td>
</tr>
<tr class="even">
<td>disable</td>
<td>Geben Sie die Warnungen nicht mit den angegebenen Zahlen aus.</td>
</tr>
<tr class="odd">
<td>error</td>
<td>Melden Sie die Warnungen mit den angegebenen Zahlen als Fehler.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>Warnung-Number-List</em></p></td>
<td><p>Eine durch Leerzeichen getrennte Liste mit den Zahlen der Warnungen, um das Verhalten von zu ändern.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Sie können eine beliebige Anzahl unterschiedlicher Änderungen an einem Warnungs Verhalten innerhalb desselben Warnungs-Pragmas angeben, indem Sie die Änderungen durch Semikolons trennen.

Der Compiler fügt 4000 einer beliebigen Warnungs Zahl zwischen 0 und 999 hinzu. Bei Warn Zahlen, die größer als 4699 sind (die der Codegenerierung zugeordneten), hat das warning-Pragma nur Auswirkungen, wenn Sie außerhalb von Funktionsdefinitionen platziert werden. Das Pragma wird ignoriert, wenn es eine Zahl größer als 4699 angibt und innerhalb einer Funktion verwendet wird.

Das HLSL Warning-Pragma unterstützt die **Push** -und **Pop** -Funktionalität des Warning-Pragmas, das im C++-Compiler enthalten ist, nicht.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden die Warnungen 4507 und 4034 deaktiviert, die Warnung 4385 einmal angezeigt und die Warnung 4164 als Fehlermeldung ausgegeben.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



Das vorherige Beispiel ist funktional äquivalent zu folgendem:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





