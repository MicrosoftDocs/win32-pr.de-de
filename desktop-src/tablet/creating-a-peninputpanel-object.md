---
description: Hier wird beschrieben, wie ein "pinputpanel"-Objekt erstellt wird
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Erstellen eines "pinputpanel"-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346040"
---
# <a name="creating-a-peninputpanel-object"></a>Erstellen eines "pinputpanel"-Objekts

\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch " [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) " und " [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))" ersetzt. Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]

Verwaltete Codekonstruktoren stellen eine bequeme Möglichkeit dar, ein " [tzinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt zu erstellen und es in einem Schritt an ein Steuerelement anzufügen. In diesem C \# -Beispiel wird ein "tzinputpanel"-Objekt erstellt und an ein vorhandenes [InkEdit](/previous-versions/ms835842(v=msdn.10)) -Steuerelement `InkEdit1` mit einer Codezeile angefügt.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



Das gleiche Beispiel in Visual Basic .net sieht wie folgt aus:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Diese Technik ist in Fällen nützlich, in denen ein " [pinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt mit einem einzelnen Steuerelement während seiner gesamten Lebensdauer verknüpft wird. Wenn Sie ein "pinputpanel"-Objekt verwenden und es mehreren Steuerelementen zuordnen möchten (wie im Beispiel " [tainputpanel](peninputpanel-sample.md)" gezeigt), verwenden Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) ", um das Steuerelement zu ändern, dem das Objekt "pinputpanel" zugeordnet ist.

Verwenden Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) ", um ein " [pinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt an ein Steuerelement ohne Verwendung eines Konstruktors anzufügen. Verwenden Sie dieses Verfahren für Sprachen, die verwaltete Konstruktoren (z. b. C++) nicht unterstützen.

 

 
