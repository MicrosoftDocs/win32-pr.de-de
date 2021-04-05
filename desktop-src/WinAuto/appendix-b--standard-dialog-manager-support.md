---
title: Anhang B-Unterstützung für Standard Dialogfelder
description: Microsoft Active Accessibility bietet umfassende Unterstützung für SDM-Dialogfeld-Steuerelemente (Standard Dialogfeld-Manager).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710866"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="d69c7-103">Anhang B: Unterstützung von Standard Dialog-Manager</span><span class="sxs-lookup"><span data-stu-id="d69c7-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="d69c7-104">Microsoft Active Accessibility bietet umfassende Unterstützung für SDM-Dialogfeld-Steuerelemente (Standard Dialogfeld-Manager).</span><span class="sxs-lookup"><span data-stu-id="d69c7-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="d69c7-105">SDM ist eine interne Microsoft-Code Bibliothek, mit der Microsoft-Anwendungen ein gewisses Maß an Unabhängigkeit von den Unterschieden zwischen Macintosh-und Microsoft Windows-Betriebssystemen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d69c7-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="d69c7-106">SDM wird hauptsächlich für Dialogfelder in Microsoft Excel und Microsoft Word verwendet.</span><span class="sxs-lookup"><span data-stu-id="d69c7-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="d69c7-107">SDM stellt Probleme für Barrierefreiheits Hilfen dar, da es nicht standardmäßige Implementierungen von Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="d69c7-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="d69c7-108">Beispielsweise verwenden SDM-Dialogfeld Schaltflächen keine Fenster Handles auf die gleiche Weise wie die standardmäßigen Benutzeroberflächen Elemente.</span><span class="sxs-lookup"><span data-stu-id="d69c7-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="d69c7-109">Sie können keine Nachrichten an Schaltflächen senden, und Schaltflächen sind nicht in der Fensterliste enthalten.</span><span class="sxs-lookup"><span data-stu-id="d69c7-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="d69c7-110">Eine Anwendung, die SDM verwendet, kommuniziert über eine private Schnittstelle mit dem-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d69c7-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="d69c7-111">Die folgende Abbildung zeigt ein Beispiel Dialogfeld aus Word.</span><span class="sxs-lookup"><span data-stu-id="d69c7-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="d69c7-112">Obwohl es sich um ein normales Windows-Dialogfeld handelt, das das Registerkarten-Steuerelement verwendet, handelt es sich tatsächlich um ein SDM-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d69c7-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![Screenshot des Dialog Felds "Optionen" mit ausgewählter Registerkarte "Ansicht"](images/dialog.gif)

 

 




