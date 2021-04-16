---
description: Verwenden Sie nach Möglichkeit standardmäßige Windows-Steuerelemente, da Sie vollständig mit den Microsoft-Active Accessibility Richtlinien kompatibel sind. Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der allgemeinen Windows-Steuerelement Bibliothek (Comctl32.dll) bereitgestellt werden.
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Verwenden von Windows-Standard Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343288"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="d569e-104">Verwenden von Windows-Standard Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d569e-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="d569e-105">Verwenden Sie nach Möglichkeit standardmäßige Windows-Steuerelemente, da Sie vollständig mit den Microsoft-Active Accessibility Richtlinien kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="d569e-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="d569e-106">Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der allgemeinen Windows-Steuerelement Bibliothek (Comctl32.dll) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d569e-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="d569e-107">Jedes standardmäßige Windows-Steuerelement ist ein separates Fenster einer bestimmten Klasse, sodass die Barrierefreiheits Hilfe benachrichtigt wird, wenn der Fokus auf ein neues Steuerelement verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d569e-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="d569e-108">Die Unterstützung kann die Fenster Klasse des Steuer Elements sowie alle zusätzlichen Meldungen ermitteln, die zum Abfragen oder Ändern des Steuerelement Zustands gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d569e-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="d569e-109">Die Hilfe kann auch alle untergeordneten Steuerelemente identifizieren, die in einem übergeordneten Fenster enthalten sind, und das übergeordnete Steuerelement eines beliebigen Steuer Elements identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d569e-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="d569e-110">Einige allgemeine Steuerelemente sind äußerst flexibel und können häufig durch weniger benutzerdefinierte Steuerelemente und vom Besitzer gezeichnete Steuerelemente ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d569e-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="d569e-111">Beispielsweise kann eine Listenansicht ein vom Besitzer gezeichnetes Listenfeld ersetzen, um ein Kontrollkästchen neben jedem Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d569e-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="d569e-112">Als weiteres Beispiel kann das Schaltflächen-Steuerelement "Erweitert" sowohl Bilder als auch Text anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d569e-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="d569e-113">Zuvor erforderte dies die Verwendung eines benutzerdefinierten Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d569e-113">Previously, this required the use of a custom control.</span></span>

 

 



