---
description: Übersicht über das Text Dienst-Framework für den Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Text Dienst Framework (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351109"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="bed66-103">Text Dienst Framework (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="bed66-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="bed66-104">Wenn das [Text Dienst Framework (TSF)](../tsf/text-services-framework.md) für ein Steuerelement aktiviert ist, dem ein " [tzinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt angefügt ist, kann das "tzinputpanel"-Objekt Text direkt einfügen.</span><span class="sxs-lookup"><span data-stu-id="bed66-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="bed66-105">Wenn das Steuerelement kein Text Services-Framework (TSF) unterstützt, muss das Objekt "tzinputpanel" mithilfe der [SendInput-Funktion](/windows/win32/api/winuser/nf-winuser-sendinput) auf "Text einfügen" zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="bed66-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="bed66-106">Die Möglichkeit, Text direkt einzufügen, wird für jene, die ostasiatische Zeichen enthalten, sehr wichtig, wenn die [SendInput-Funktion](/windows/win32/api/winuser/nf-winuser-sendinput) falsche Zeichen verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="bed66-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="bed66-107">TSF stellt eine Schnittstelle zum Beheben von Erkennungs Fehlern bereit, die es dem Endbenutzer ermöglicht, den richtigen Text zu korrigieren, umzuschreiben oder sogar vorzuschreiben.</span><span class="sxs-lookup"><span data-stu-id="bed66-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="bed66-108">TSF wird aktiviert, indem die [enabletsf](/previous-versions/ms569656(v=vs.100)) -Methode aufgerufen wird, wobei der *enable* -Parameter auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bed66-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="bed66-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="bed66-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="bed66-110">Ein an ein [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelement angefügtes " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt bietet eine robuste Benutzer Leistung, da die InkEdit TSF unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bed66-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="bed66-111">Stellen Sie jedoch sicher, dass die Eigenschaft [InkMode](/previous-versions/ms835850(v=msdn.10)) auf [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) festgelegt ist, wie im Thema [bewährte Methoden](best-practices.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bed66-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="bed66-112">Das Beispiel " [tainputpanel](peninputpanel-sample.md) " enthält ein Beispiel für die Aktivierung von TSF.</span><span class="sxs-lookup"><span data-stu-id="bed66-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bed66-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bed66-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bed66-114">Textdienstframework</span><span class="sxs-lookup"><span data-stu-id="bed66-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
