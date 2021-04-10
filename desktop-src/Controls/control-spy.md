---
title: Control Spy v 2.0
description: Control Spy ist ein Tool, mit dem Entwickler allgemeine Steuerelemente verstehen können, wie Sie Stile auf Sie anwenden und wie Sie auf Nachrichten und Benachrichtigungen reagieren.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039774"
---
# <a name="control-spy-v20"></a><span data-ttu-id="d7ee9-103">Control Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="d7ee9-103">Control Spy v2.0</span></span>

<span data-ttu-id="d7ee9-104">Control Spy ist ein Tool, mit dem Entwickler allgemeine Steuerelemente verstehen können: wie Sie Stile auf Sie anwenden und wie Sie auf Nachrichten und Benachrichtigungen reagieren.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="d7ee9-105">Mithilfe von Control Spy können Sie sofort sehen, wie sich unterschiedliche Stile auf das Verhalten und die Darstellung der einzelnen Steuerelemente auswirken, und wie Sie den Zustand der einzelnen Steuerelemente ändern können, indem Sie Nachrichten senden.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="d7ee9-106">Es sind zwei Versionen von Control Spy verfügbar: eine für [Comctl32.dll Version 5. x](common-control-versions.md) und eine für Comctl32.dll Version 6,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="d7ee9-107">ControlSpyV6.exe verfügt über ein integriertes Anwendungs Manifest, das die neueren Steuerelemente mit dem Design "Design" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="d7ee9-108">ControlSpyV5.exe nicht über dieses Manifest verfügt und somit standardmäßig die ältere Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="d7ee9-109">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d7ee9-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d7ee9-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d7ee9-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="d7ee9-111">Stile</span><span class="sxs-lookup"><span data-stu-id="d7ee9-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="d7ee9-112">Meldungen</span><span class="sxs-lookup"><span data-stu-id="d7ee9-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="d7ee9-113">Größe/Farbe</span><span class="sxs-lookup"><span data-stu-id="d7ee9-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="d7ee9-114">Speicherort des Steuerungs Spy</span><span class="sxs-lookup"><span data-stu-id="d7ee9-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="d7ee9-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7ee9-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d7ee9-116">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d7ee9-116">Overview</span></span>

<span data-ttu-id="d7ee9-117">Control Spy hostet ein ausgewähltes gemeinsames Steuerelement in der Mitte des Anwendungsfensters.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="d7ee9-118">Sie können das angezeigte Steuerelement ändern, indem Sie im Listenfeld auf der linken Seite des Fensters verschiedene Steuerelemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="d7ee9-119">Nachrichten oder Benachrichtigungen, die vom Steuerelement empfangen werden, werden auf der rechten Seite des Fensters angezeigt, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="d7ee9-120">Sie können diese Funktion aktivieren oder deaktivieren, indem Sie die Kontrollkästchen empfangene **Nachrichten** und **empfangene Benachrichtigungen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="d7ee9-121">Die folgende Abbildung zeigt die Spy-Steuerungsanwendung.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-121">The following image shows the Control Spy application.</span></span>

![Spy-Fenster steuern](images/controlspy-main.png)

<span data-ttu-id="d7ee9-123">Am unteren Rand des Fensters stehen mehrere Registerkarten zur Verfügung, die mehr Funktionalität enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="d7ee9-124">Stile</span><span class="sxs-lookup"><span data-stu-id="d7ee9-124">Styles</span></span>

<span data-ttu-id="d7ee9-125">Auf der Registerkarte **Stile** können Sie den aktuellen Fenster Stil des Steuer Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="d7ee9-126">Wählen Sie einen der aufgelisteten Stile aus bzw. deaktivieren Sie diese, und klicken Sie dann auf die Schaltfläche übernehmen, **um die Art** des angezeigten Steuer Elements zu ändern</span><span class="sxs-lookup"><span data-stu-id="d7ee9-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="d7ee9-127">Alternativ können Sie die **Schaltfläche neu erstellen verwenden** , um ein neues Steuerelement mit den ausgewählten Stilen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="d7ee9-128">Mit der Schaltfläche **Zurücksetzen** wird das Steuerelement an die Standard Stile zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="d7ee9-129">Die Schaltflächen zum **Kopieren** **und Kopieren der** Schaltflächen unterhalb der Registerkarte kopieren die ausgewählten Format Konstanten als bitweise oder ()-Trennzeichen in die Zwischenablage \| .</span><span class="sxs-lookup"><span data-stu-id="d7ee9-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="d7ee9-130">Sie können diese Liste direkt in ihren aufzurufenden Befehl anfügen, um ein Steuerelement in ihrer eigenen Anwendung mit demselben Stil [**bereitzustellen.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)</span><span class="sxs-lookup"><span data-stu-id="d7ee9-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="d7ee9-131">Die folgende Abbildung zeigt die Registerkarte **Stile** für ein Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-131">The following image shows the **Styles** tab for a button control.</span></span>

![Registerkarte "Spy Stile Steuern"](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="d7ee9-133">Meldungen</span><span class="sxs-lookup"><span data-stu-id="d7ee9-133">Messages</span></span>

<span data-ttu-id="d7ee9-134">Auf der Registerkarte **Nachrichten** können Sie nahezu jede Nachricht an ein Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="d7ee9-135">Nachdem Sie eine Nachricht aus dem Listenfeld ausgewählt haben, können Sie Daten eingeben, die als *wParam* -Parameter und *LPARAM* -Parameter des Aufrufes [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="d7ee9-136">Nachdem Sie auf **senden** klicken, wird die Meldung an das Steuerelement gesendet, und im Textfeld unten auf der Registerkarte wird ein beliebiges Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="d7ee9-137">In der folgenden Abbildung wird die Registerkarte Nachrichten angezeigt, wenn eine bestimmte Nachricht ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-137">The following image shows the messages tab when a particular message is selected.</span></span>

![Registerkarte "Spy Messages" Steuern](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="d7ee9-139">Größe/Farbe</span><span class="sxs-lookup"><span data-stu-id="d7ee9-139">Size/Color</span></span>

<span data-ttu-id="d7ee9-140">Die Registerkarte **Größe/Farbe** kann verwendet werden, um die Größe des Steuer Elements und die Farbe seines Hintergrunds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="d7ee9-141">Speicherort des Steuerungs Spy</span><span class="sxs-lookup"><span data-stu-id="d7ee9-141">Where to Get Control Spy</span></span>

<span data-ttu-id="d7ee9-142">Sie können [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) von MSDN herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="d7ee9-143">Beide Versionen sind im Download enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7ee9-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7ee9-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7ee9-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d7ee9-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d7ee9-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7ee9-146">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d7ee9-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="d7ee9-147">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="d7ee9-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 