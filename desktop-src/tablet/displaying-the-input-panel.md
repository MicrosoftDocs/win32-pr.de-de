---
description: Übersicht über die Anzeige des Eingabebereichs.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Anzeigen des Eingabebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940790"
---
# <a name="displaying-the-input-panel"></a>Anzeigen des Eingabebereichs

\[[**PenInputPanel**](peninputpanel-class.md) wurde durch [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ersetzt ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) für verwalteten Code). Weitere Informationen finden Sie unter [Programmieren des Texteingabebereichs.](programming-the-text-input-panel.md)\]

Die Reihenfolge der verschiedenen Fokusereignisse für ein Steuerelement lautet wie folgt:

-   [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control.Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control.Validating](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control.Validated](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control.LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Es gibt keine Garantie dafür, dass das Steuerelement tatsächlich den Fokus besitzt, wenn die [Control.Visible-Eigenschaft](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) geschrieben wird, wenn es im [Control.Enter-Ereignishandler](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) festgelegt wird. Das Control.Enter-Ereignis ist der beste Ort, um das [PenInputPanel-Objekt](/previous-versions/ms583923(v=vs.100)) an ein Steuerelement anzufügen, aber das [Control.GotFocus-Ereignis](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) ist der beste Ort, um die [PenInputPanel.Visible-Eigenschaft](/previous-versions/ms571984(v=vs.100)) zu ändern.

 

 
