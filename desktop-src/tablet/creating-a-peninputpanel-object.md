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
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="d12ac-103">Erstellen eines "pinputpanel"-Objekts</span><span class="sxs-lookup"><span data-stu-id="d12ac-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="d12ac-104">\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch " [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) " und " [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d12ac-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="d12ac-105">Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]</span><span class="sxs-lookup"><span data-stu-id="d12ac-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="d12ac-106">Verwaltete Codekonstruktoren stellen eine bequeme Möglichkeit dar, ein " [tzinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt zu erstellen und es in einem Schritt an ein Steuerelement anzufügen.</span><span class="sxs-lookup"><span data-stu-id="d12ac-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="d12ac-107">In diesem C \# -Beispiel wird ein "tzinputpanel"-Objekt erstellt und an ein vorhandenes [InkEdit](/previous-versions/ms835842(v=msdn.10)) -Steuerelement `InkEdit1` mit einer Codezeile angefügt.</span><span class="sxs-lookup"><span data-stu-id="d12ac-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="d12ac-108">Das gleiche Beispiel in Visual Basic .net sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d12ac-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="d12ac-109">Diese Technik ist in Fällen nützlich, in denen ein " [pinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt mit einem einzelnen Steuerelement während seiner gesamten Lebensdauer verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="d12ac-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="d12ac-110">Wenn Sie ein "pinputpanel"-Objekt verwenden und es mehreren Steuerelementen zuordnen möchten (wie im Beispiel " [tainputpanel](peninputpanel-sample.md)" gezeigt), verwenden Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) ", um das Steuerelement zu ändern, dem das Objekt "pinputpanel" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d12ac-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="d12ac-111">Verwenden Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) ", um ein " [pinputpanel](/previous-versions/ms583923(v=vs.100)) "-Objekt an ein Steuerelement ohne Verwendung eines Konstruktors anzufügen.</span><span class="sxs-lookup"><span data-stu-id="d12ac-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="d12ac-112">Verwenden Sie dieses Verfahren für Sprachen, die verwaltete Konstruktoren (z. b. C++) nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d12ac-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 
