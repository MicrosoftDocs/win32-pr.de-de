---
description: Übersicht über bewährte Methoden bei Verwendung des Stift Eingabe Panel-Objekts.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Bewährte Methoden (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218580"
---
# <a name="best-practices-tablet-pc"></a>Bewährte Methoden (Tablet PC)

Es gibt einige Richtlinien, die Sie beachten sollten, wenn Sie das Objekt " [**pinputpanel**](peninputpanel-class.md) " verwenden.

-   [InkEdit-Steuerelement bevorzugen](#prefer-inkedit-control)
-   [Freihand Modus für InkEdit-Steuerelemente deaktivieren](#disable-ink-mode-on-inkedit-controls)
-   [Verwenden von fensterlosen Steuerelementen](#using-windowless-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="prefer-inkedit-control"></a>InkEdit-Steuerelement bevorzugen

[InkEdit](inkedit-control-reference.md) ist das bevorzugte Steuerelement, an das das Objekt " [**turinputpanel**](peninputpanel-class.md) " angefügt werden soll. Das InkEdit-Steuerelement bietet Unterstützung für das [Text Services-Framework (TSF)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Freihand Modus für InkEdit-Steuerelemente deaktivieren

Legen Sie beim Anfügen an ein [InkEdit](inkedit-control-reference.md) -Steuerelement die Eigenschaft [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) des InkEdit-Steuer Elements auf den Wert [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) fest. Wenn die Eigenschaft **InkMode** nicht auf den Wert **InkMode** festgelegt ist, interpretiert das InkEdit-Steuerelement den ersten Tap als Strich, übergibt ihn an die Erkennung und fügt den Text in das InkEdit-Steuerelement ein. Da Sie bereits [**über ein "**](peninputpanel-class.md) "-Objekt verfügen, das an eine frei Hand Eingabe gebunden ist, ist es nicht erforderlich, dass das InkEdit-Steuerelement auch für die frei Hand Eingabe aktiviert ist.

## <a name="using-windowless-controls"></a>Verwenden von fensterlosen Steuerelementen

Wenn ein " [**tzinputpanel**](peninputpanel-class.md) "-Objekt an ein übergeordnetes Fenster angefügt wird, das mehr als ein fensterloses Steuerelement enthält, weiß das Objekt " **tzinputpanel** " nicht, wie die Einfügemarke nachverfolgt werden soll, wenn sich der Fokus zwischen Fenstern untergeordneten Elementen Handschrift Eingaben können an das falsche untergeordnete Element gesendet werden, wenn der Fokus von einem fensterlosen Steuerelement zu einem anderen verschoben wird, während die Eingabe aussteht.

Um das Objekt " [**pinputpanel**](peninputpanel-class.md) " in einer fensterlosen Umgebung zu verwenden, kann folgendes Verfahren verwendet werden:

1.  Instanziieren Sie ein [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) -Steuerelement, und positionieren Sie es über dem fensterlosen Steuerelement.
2.  Fügen Sie das Objekt " [**tzinputpanel**](peninputpanel-class.md) " an das neue Textfeld-Steuerelement an.
3.  Lassen Sie das Textfeld-Steuerelement den erkannten Text aus dem Objekt " [**tzinputpanel**](peninputpanel-class.md) " erfassen.
4.  Wenn sich der Fokus auf das Textfeld-Steuerelement ändert, wird die [**commitpdinginput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) -Methode des " [**tzinputpanel**](peninputpanel-class.md) "-Objekts aufgerufen.
5.  Kopieren Sie den erkannten Text aus dem Textfeld-Steuerelement in das untergeordnete Fenster.
6.  Trennen Sie das Objekt " [**pinputpanel**](peninputpanel-class.md) ", indem Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) " (nur verwalteter Code) oder die Eigenschaft " [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) " auf NULL festlegen.
7.  Löschen Sie das Textfeld-Steuerelement.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Pinputpanel-Klasse**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. pinputpanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Textdienstframework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
