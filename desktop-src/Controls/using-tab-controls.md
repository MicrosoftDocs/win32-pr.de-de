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
# <a name="using-tab-controls"></a><span data-ttu-id="631fb-103">Verwenden von Register Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="631fb-103">Using Tab Controls</span></span>

<span data-ttu-id="631fb-104">Dieses Thema enthält zwei Beispiele, die Registerkarten-Steuerelemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="631fb-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="631fb-105">Im ersten Beispiel wird veranschaulicht, wie ein Registerkarten-Steuerelement verwendet wird, um zwischen mehreren Seiten von Text im Hauptfenster einer Anwendung zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="631fb-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="631fb-106">Im zweiten Beispiel wird veranschaulicht, wie ein Registerkarten-Steuerelement verwendet wird, um zwischen mehreren Seiten von Steuerelementen in einem Dialogfeld zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="631fb-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="631fb-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="631fb-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="631fb-108">Thema</span><span class="sxs-lookup"><span data-stu-id="631fb-108">Topic</span></span></th>
<th><span data-ttu-id="631fb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="631fb-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="631fb-110"><a href="create-a-tab-control-in-the-main-window.md">Erstellen eines Registerkarten-Steuer Elements im Hauptfenster</a></span><span class="sxs-lookup"><span data-stu-id="631fb-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="631fb-111">Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Registerkarten-Steuerelement erstellt und im Client Bereich des Hauptfensters der Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="631fb-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="631fb-112">Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkarten-Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="631fb-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="631fb-113">Das übergeordnete Fenster positioniert und passt das Registerkarten-Steuerelement und das statische Steuerelement an, wenn es die <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="631fb-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="631fb-114">In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche.</span><span class="sxs-lookup"><span data-stu-id="631fb-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="631fb-115">Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tags im statischen Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="631fb-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="631fb-116"><a href="create-a-tabbed-dialog-box.md">Erstellen eines Dialog Felds im Registerkarten Format</a></span><span class="sxs-lookup"><span data-stu-id="631fb-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="631fb-117">Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Dialogfeld erstellt wird, in dem Registerkarten verwendet werden, um mehrere Seiten von Steuerelementen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="631fb-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="631fb-118">Das Haupt Dialogfeld ist ein modales Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="631fb-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="631fb-119">Jede Seite von Steuerelementen wird durch eine Dialogfeld Vorlage definiert, die den <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="631fb-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="631fb-120">Wenn eine Registerkarte ausgewählt ist, wird ein nicht modalem Dialogfeld für die eingehende Seite erstellt, und das Dialogfeld für die ausgehende Seite wird zerstört.</span><span class="sxs-lookup"><span data-stu-id="631fb-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="631fb-121">In vielen Fällen können Sie mithilfe von Eigenschaften Blättern leichter Dialogfelder mit mehreren Seiten implementieren.</span><span class="sxs-lookup"><span data-stu-id="631fb-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="631fb-122">Weitere Informationen zu Eigenschaften Blättern finden Sie unter Informationen <a href="property-sheets.md">zu Eigenschaften Blättern</a>.</span><span class="sxs-lookup"><span data-stu-id="631fb-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="631fb-123">Mit der Vorlage für das Haupt Dialogfeld werden lediglich zwei Schaltflächen-Steuerelemente definiert.</span><span class="sxs-lookup"><span data-stu-id="631fb-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="631fb-124">Wenn Sie die <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> Nachricht verarbeiten, erstellt die Dialogfeld Prozedur ein Registerkarten-Steuerelement und lädt die Dialogfeld Vorlagen Ressourcen für jedes der untergeordneten Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="631fb-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

