---
title: Syntaxunterschiede
description: Die offensichtlichste Änderung bei der Umstellung zwischen Programmiersprachen ist die Syntax Änderung.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474349"
---
# <a name="syntax-differences"></a>Syntaxunterschiede

Die offensichtlichste Änderung bei der Umstellung zwischen Programmiersprachen ist die Syntax Änderung.

Sehen Sie sich die Add-Methode des enhevents-Objekts an, die wie in drei verschiedenen Sprachen deklariert ist.

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

Obwohl die Syntax der einzelnen Sprachen die Methode anders ausdrückt, ist die Funktionalität identisch. In jeder Sprache übernimmt die Add-Methode die Parameter *time* und *Name* und gibt ein enhevent-Objekt zurück. Im C++-Beispiel gibt die-Methode das-Objekt mithilfe eines dritten Output-Parameters ( *PVal*) zurück.

In der Regel ist die Funktionalität eines COM-Objekts in den Programmiersprachen identisch. Aus diesem Grund ist die Dokumentation für ein COM-Objekt auch dann nützlich, wenn das Objekt in einer anderen Programmiersprache dokumentiert ist als das, das Sie verwenden. Die Beschreibungen der Funktionen, Parameter und Rückgabewerte des Objekts sind mit wenigen Ausnahmen, die für alle Sprachen gültig sind.

Informationen dazu, wie Sie die Syntax eines COM-Objekts in eine andere Programmiersprache konvertieren, finden Sie unter über [setzen der COM-Objekt Syntax für Programmiersprachen](translating-com-object-syntax-for-programming-languages.md).

Die Syntax Unterschiede zwischen den Skriptsprachen Javascript, JScript und VBScript sind weniger ausgeprägt als die Syntax Unterschiede zwischen den oben gezeigten Programmiersprachen. Sehen Sie sich beispielsweise die quadratische Funktion an, wie Sie in jeder dieser drei Skriptsprachen implementiert wird:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Beachten Sie, dass die Skriptsprachen im Gegensatz zu den Programmiersprachen schwach typisiert sind. Anders ausgedrückt: Sie müssen den Datentyp eines Parameters oder Rückgabewerts nicht angeben, wenn Sie eine Funktion deklarieren. Stattdessen werden die Variablen automatisch in den entsprechenden Datentyp umgewandelt. Im Fall von VBScript weisen alle Variablen denselben Datentyp auf, **Variant**.

Die JavaScript-und JScript-Syntax für Square ist identisch. JScript ist größtenteils mit JavaScript kompatibel. JScript enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. **ActiveXObject**, **Enumerator**, **Error**, **Global** und **VBArray**. Weitere Informationen zu diesen Objekten finden Sie in der [JScript-Sprachreferenz](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

Auf der Oberfläche ähnelt die JavaScript-und JScript-Syntax der Java-Syntax. Diese Ähnlichkeit ist nur oberflächlich. Die Java-Sprache wurde unabhängig von JavaScript und JScript entwickelt und steht nicht im Zusammenhang mit beiden.

VBScript hingegen ist eine Teilmenge der Programmiersprache Visual Basic. Aus diesem Grund ist die VBScript-Syntax eine Teilmenge Visual Basic Syntax und häufig mit Visual Basic Syntax austauschbar.

Informationen zur Verwendung von COM-Objekten in Skriptsprachen finden Sie unter [Skripterstellung mit COM-Objekten](scripting-with-com-objects.md).

 

 