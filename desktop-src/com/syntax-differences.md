---
title: Syntaxunterschiede
description: Die offensichtlichste Änderung beim Wechsel zwischen Programmiersprachen ist die Änderung der Syntax.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef58f92bf87d877c2c55a73fe5f717b93c359119e5ca6aa73fc1aeee531d858
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678390"
---
# <a name="syntax-differences"></a>Syntaxunterschiede

Die offensichtlichste Änderung beim Wechsel zwischen Programmiersprachen ist die Änderung der Syntax.

Betrachten Sie die Add-Methode des EnhEvents-Objekts, die in drei verschiedenen Sprachen deklariert ist.

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

Obwohl die Syntax der einzelnen Sprachen die Methode anders ausdrückt, ist die Funktionalität identisch. In jeder Sprache verwendet die Add-Methode die Parameter *Time* und *Name* und gibt ein EnhEvent-Objekt zurück. Im C++-Beispiel gibt die -Methode das -Objekt mithilfe des dritten Ausgabeparameters *pVal zurück.*

In der Regel ist die Funktionalität eines COM-Objekts programmiersprachenübergreifend identisch. Aus diesem Grund ist die Dokumentation für ein COM-Objekt nützlich, auch wenn das Objekt in einer anderen Programmiersprache als der von Ihnen verwendet dokumentiert ist. Die Beschreibungen der Funktionen, Parameter und Rückgabewerte des Objekts sind bis auf wenige Ausnahmen für alle Sprachen gültig.

Informationen zum Konvertieren der Syntax eines COM-Objekts in eine andere Programmiersprache finden Sie unter [Übersetzen der COM-Objektsyntax für Programmiersprachen](translating-com-object-syntax-for-programming-languages.md).

Die Syntaxunterschiede zwischen den Skriptsprachen JavaScript, JScript und VBScript sind weniger deutlich als die Syntaxunterschiede zwischen den oben gezeigten Programmiersprachen. Betrachten Sie beispielsweise die square-Funktion, da sie in jeder dieser drei Skriptsprachen implementiert ist:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Beachten Sie, dass die Skriptsprachen im Gegensatz zu den Programmiersprachen schwach typiert sind. Anders ausgedrückt: Sie müssen den Datentyp eines Parameters oder Rückgabewerts nicht angeben, wenn Sie eine Funktion deklarieren. Stattdessen werden die Variablen automatisch in den entsprechenden Datentyp castiert. Im Fall von VBScript haben alle Variablen denselben Datentyp, **Variant**.

Die JavaScript- JScript-Syntax für square ist identisch. JScript ist größtenteils mit JavaScript kompatibel. Allerdings enthält JScript objekte, die derzeit nicht von JavaScript unterstützt werden, z. B. **ActiveXObject**, **Enumerator**, **Error**, **Global** und **VBArray**. Weitere Informationen zu diesen Objekten finden Sie in der JScript [Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

Die JavaScript- und JScript ähneln der Java-Syntax. Diese Ähnlichkeit ist nur lässig. Die Java-Sprache wurde unabhängig von JavaScript und JScript und ist mit beiden nicht verknüpft.

VBScript ist dagegen eine Teilmenge der Visual Basic Programmiersprache. Aus diesem Grund ist die VBScript-Syntax eine Teilmenge Visual Basic Syntax und kann häufig mit Visual Basic werden.

Informationen zur Verwendung von COM-Objekten in Skriptsprachen finden Sie unter [Skripterstellung mit COM-Objekten.](scripting-with-com-objects.md)

 

 