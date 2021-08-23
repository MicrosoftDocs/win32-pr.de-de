---
description: Beschreibt, wie ein PenInputPanel-Objekt erstellt wird.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Erstellen eines PenInputPanel-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e1c54bd8555521cae00fe10c70f8980d7d8b6a5d17d810d90b945feacece8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395288"
---
# <a name="creating-a-peninputpanel-object"></a>Erstellen eines PenInputPanel-Objekts

\[[**PenInputPanel**](peninputpanel-class.md) wurde durch [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) und [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))ersetzt. Weitere Informationen finden Sie unter [Programmieren des Texteingabebereichs.](programming-the-text-input-panel.md)\]

Verwaltete Codekonstruktoren bieten eine praktische Möglichkeit, ein [PenInputPanel-Objekt](/previous-versions/ms583923(v=vs.100)) zu erstellen und es in einem Schritt an ein Steuerelement anzufügen. In diesem \# C-Beispiel wird ein PenInputPanel-Objekt erstellt und mit einer Codezeile an ein vorhandenes [InkEdit-Steuerelement](/previous-versions/ms835842(v=msdn.10)) `InkEdit1` angefügt.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



Das gleiche Beispiel in Visual Basic .NET sieht wie folgt aus:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Diese Technik ist nützlich in Fällen, in denen ein [PenInputPanel-Objekt](/previous-versions/ms583923(v=vs.100)) einem einzelnen Steuerelement während seiner gesamten Lebensdauer zugeordnet wird. Wenn Sie ein PenInputPanel-Objekt verwenden und es mehreren Steuerelementen zuordnen möchten, wie im [PenInputPanel-Beispiel](peninputpanel-sample.md)gezeigt, verwenden Sie die [AttachedEditControl-Eigenschaft,](/previous-versions/ms582239(v=vs.100)) um das Steuerelement zu ändern, dem das PenInputPanel-Objekt zugeordnet ist.

Um ein [PenInputPanel-Objekt](/previous-versions/ms583923(v=vs.100)) ohne Konstruktor an ein Steuerelement anzufügen, verwenden Sie die [AttachedEditControl-Eigenschaft.](/previous-versions/ms582239(v=vs.100)) Verwenden Sie dieses Verfahren für Sprachen, die die verwalteten Konstruktoren nicht unterstützen, z. B. C++.

 

 
