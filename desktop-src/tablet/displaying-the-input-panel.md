---
description: Übersicht über das Anzeigen des Eingabe Bereichs.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Anzeigen des Eingabe Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362774"
---
# <a name="displaying-the-input-panel"></a>Anzeigen des Eingabe Bereichs

\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch " [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) " ersetzt ("[Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) " für verwalteten Code). Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]

Die Reihenfolge der verschiedenen Fokus Ereignisse für ein Steuerelement lautet wie folgt:

-   [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control. validieren](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control. validiert](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Es gibt keine Garantie, dass das Steuerelement den Fokus tatsächlich um den Zeitpunkt hat, zu dem die [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) -Eigenschaft geschrieben wird, wenn Sie im [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) -Ereignishandler festgelegt wird. Das Steuerelement. Enter-Ereignis ist der beste Ort, um [das Objekt "](/previous-versions/ms583923(v=vs.100)) " "" "" "" "" "" "" " [".](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) [](/previous-versions/ms571984(v=vs.100))

 

 
