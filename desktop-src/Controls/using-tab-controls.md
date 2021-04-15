---
title: Verwenden von Register Steuerelementen
description: Dieses Thema enthält zwei Beispiele, die Registerkarten-Steuerelemente verwenden.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474509"
---
# <a name="using-tab-controls"></a>Verwenden von Register Steuerelementen

Dieses Thema enthält zwei Beispiele, die Registerkarten-Steuerelemente verwenden. Im ersten Beispiel wird veranschaulicht, wie ein Registerkarten-Steuerelement verwendet wird, um zwischen mehreren Seiten von Text im Hauptfenster einer Anwendung zu wechseln. Im zweiten Beispiel wird veranschaulicht, wie ein Registerkarten-Steuerelement verwendet wird, um zwischen mehreren Seiten von Steuerelementen in einem Dialogfeld zu wechseln.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-a-tab-control-in-the-main-window.md">Erstellen eines Registerkarten-Steuer Elements im Hauptfenster</a><br/></td>
<td>Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Registerkarten-Steuerelement erstellt und im Client Bereich des Hauptfensters der Anwendung angezeigt wird. Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkarten-Steuer Elements an. Das übergeordnete Fenster positioniert und passt das Registerkarten-Steuerelement und das statische Steuerelement an, wenn es die <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> Nachricht verarbeitet. <br/> In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche. Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tags im statischen Steuerelement an. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Erstellen eines Dialog Felds im Registerkarten Format</a><br/></td>
<td>Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Dialogfeld erstellt wird, in dem Registerkarten verwendet werden, um mehrere Seiten von Steuerelementen bereitzustellen. Das Haupt Dialogfeld ist ein modales Dialogfeld. Jede Seite von Steuerelementen wird durch eine Dialogfeld Vorlage definiert, die den <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> Stil aufweist. Wenn eine Registerkarte ausgewählt ist, wird ein nicht modalem Dialogfeld für die eingehende Seite erstellt, und das Dialogfeld für die ausgehende Seite wird zerstört. <br/>
<blockquote>
[!Note]<br />
In vielen Fällen können Sie mithilfe von Eigenschaften Blättern leichter Dialogfelder mit mehreren Seiten implementieren. Weitere Informationen zu Eigenschaften Blättern finden Sie unter Informationen <a href="property-sheets.md">zu Eigenschaften Blättern</a>.
</blockquote>
<br/> Mit der Vorlage für das Haupt Dialogfeld werden lediglich zwei Schaltflächen-Steuerelemente definiert. Wenn Sie die <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> Nachricht verarbeiten, erstellt die Dialogfeld Prozedur ein Registerkarten-Steuerelement und lädt die Dialogfeld Vorlagen Ressourcen für jedes der untergeordneten Dialogfelder. <br/></td>
</tr>
</tbody>
</table>



 

