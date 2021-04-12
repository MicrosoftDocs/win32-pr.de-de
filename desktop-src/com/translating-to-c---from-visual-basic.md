---
title: Übersetzen in C++ von Visual Basic
description: Visual Basic behandelt Zeiger implizit. In C++ ist Ihre Anwendung für die Ausführung erforderlicher Zeigerarithmetik verantwortlich.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206717"
---
# <a name="translating-to-c-from-visual-basic"></a>Übersetzen in C++ von Visual Basic

Visual Basic behandelt Zeiger implizit. In C++ ist Ihre Anwendung für die Ausführung erforderlicher Zeigerarithmetik verantwortlich.

Standardmäßig übergibt Visual Basic Parameter nach Verweis (als Zeiger). Parameter, die nur als Wert übermittelt werden sollen, werden durch das Schlüsselwort **ByVal** angegeben. Beispielsweise entspricht der  **ganzzahlige** Parameter " **ByVal**" in Visual Basic einem **kurzen** Parameter in C++, wohingegen ein **ByRef**- **Parameter in** Visual Basic einem **kurzen \*** Parameter entspricht.

Ein Parameter, der in Visual Basic **als Zeichenfolge** deklariert ist, wird als Zeiger auf einen **BSTR** in C++ deklariert. Das Festlegen eines Zeichen folgen Zeigers auf **null** in C++ entspricht dem Festlegen der Zeichenfolge auf die **vbNullString** -Konstante in Visual Basic. Das übergeben einer Zeichenfolge der Länge 0 (null) an eine Funktion, die für den Empfang von **null** vorgesehen ist, funktioniert nicht, da dadurch ein Zeiger auf eine Zeichenfolge der Länge 0 (null) anstatt auf einen NULL-Zeiger übergeben wird.

C++ und Visual Basic unterscheiden sich geringfügig von der Darstellung von Eigenschaften. In C++ werden Eigenschaften als ein Satz von Accessorfunktionen dargestellt, der den Eigenschafts Wert festlegt und einen, der den Eigenschafts Wert abruft. In Visual Basic werden Eigenschaften als einzelnes Element dargestellt, das zum Abrufen oder Festlegen des Eigenschafts Werts verwendet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> </dl>

 

 




