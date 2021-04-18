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
# <a name="text-services-framework-tablet-pc"></a>Text Dienst Framework (Tablet PC)

Wenn das [Text Dienst Framework (TSF)](../tsf/text-services-framework.md) für ein Steuerelement aktiviert ist, dem ein " [tzinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt angefügt ist, kann das "tzinputpanel"-Objekt Text direkt einfügen. Wenn das Steuerelement kein Text Services-Framework (TSF) unterstützt, muss das Objekt "tzinputpanel" mithilfe der [SendInput-Funktion](/windows/win32/api/winuser/nf-winuser-sendinput) auf "Text einfügen" zurückgreifen.

Die Möglichkeit, Text direkt einzufügen, wird für jene, die ostasiatische Zeichen enthalten, sehr wichtig, wenn die [SendInput-Funktion](/windows/win32/api/winuser/nf-winuser-sendinput) falsche Zeichen verursachen kann.

TSF stellt eine Schnittstelle zum Beheben von Erkennungs Fehlern bereit, die es dem Endbenutzer ermöglicht, den richtigen Text zu korrigieren, umzuschreiben oder sogar vorzuschreiben.

TSF wird aktiviert, indem die [enabletsf](/previous-versions/ms569656(v=vs.100)) -Methode aufgerufen wird, wobei der *enable* -Parameter auf **true** festgelegt ist.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Ein an ein [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelement angefügtes " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt bietet eine robuste Benutzer Leistung, da die InkEdit TSF unterstützt. Stellen Sie jedoch sicher, dass die Eigenschaft [InkMode](/previous-versions/ms835850(v=msdn.10)) auf [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) festgelegt ist, wie im Thema [bewährte Methoden](best-practices.md) beschrieben.

Das Beispiel " [tainputpanel](peninputpanel-sample.md) " enthält ein Beispiel für die Aktivierung von TSF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textdienstframework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
