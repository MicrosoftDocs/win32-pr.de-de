---
description: Dieses Ereignis wird vom scrollabletext-Steuerelement veröffentlicht, damit der Benutzer den Inhalt des Steuer Elements drucken kann.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: Msiprint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868644"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="0d2b6-103">Msiprint ControlEvent</span><span class="sxs-lookup"><span data-stu-id="0d2b6-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="0d2b6-104">Dieses Ereignis wird vom [scrollabletext-Steuer](scrollabletext-control.md) Element veröffentlicht, damit der Benutzer den Inhalt des Steuer Elements drucken kann.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="0d2b6-105">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="0d2b6-106">Dieses ControlEvent ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="0d2b6-107">Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element abonniert werden, das sich im gleichen Dialogfeld wie das [scrollabletext-Steuer](scrollabletext-control.md)Element befindet.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="0d2b6-108">In der [Tabelle "ControlEvent](controlevent-table.md)" sollte "themsiprint ControlEvent" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="0d2b6-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="0d2b6-109">Published By</span></span>

[<span data-ttu-id="0d2b6-110">Scrollabletext</span><span class="sxs-lookup"><span data-stu-id="0d2b6-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="0d2b6-111">Argument</span><span class="sxs-lookup"><span data-stu-id="0d2b6-111">Argument</span></span>

<span data-ttu-id="0d2b6-112">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0d2b6-113">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="0d2b6-113">Action on Subscribers</span></span>

<span data-ttu-id="0d2b6-114">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0d2b6-115">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="0d2b6-115">Typical Use</span></span>

<span data-ttu-id="0d2b6-116">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen Dialogfeld wie das [scrollabletext-Steuer](scrollabletext-control.md) Element kann verwendet werden, um ein modales Dialogfeld anzuzeigen, das es dem Benutzer ermöglicht, den Inhalt des scrollabletext-Steuer Elements zu drucken.</span><span class="sxs-lookup"><span data-stu-id="0d2b6-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



