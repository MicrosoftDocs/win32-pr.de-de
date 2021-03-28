---
description: Mit einem übergeordneten Gerätekontext kann eine Anwendung die Zeit minimieren, die zum Einrichten des Clippingbereichs für ein Fenster erforderlich ist.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Übergeordnete Geräte Kontexte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978441"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="ec396-103">Übergeordnete Geräte Kontexte anzeigen</span><span class="sxs-lookup"><span data-stu-id="ec396-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="ec396-104">Mit einem über *geordneten Gerätekontext* kann eine Anwendung die Zeit minimieren, die zum Einrichten des Clippingbereichs für ein Fenster erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ec396-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="ec396-105">Eine Anwendung verwendet in der Regel übergeordnete Geräte Kontexte, um das Zeichnen von Steuerungs Fenstern zu beschleunigen, ohne einen privaten oder Klassen Gerätekontext zu erfordern.</span><span class="sxs-lookup"><span data-stu-id="ec396-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="ec396-106">Beispielsweise verwendet das System die übergeordneten Geräte Kontexte für die Schaltfläche Push-Schaltfläche und Bearbeitungs Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="ec396-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="ec396-107">Übergeordnete Geräte Kontexte sind nur für die Verwendung mit untergeordneten Fenstern gedacht, niemals mit den Fenstern der obersten Ebene oder des Popup Fensters.</span><span class="sxs-lookup"><span data-stu-id="ec396-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="ec396-108">Eine Anwendung kann den CS- \_ parametrientdc-Stil angeben, um den Ausschneide Bereich des untergeordneten Fensters auf die des übergeordneten Fensters festzulegen, damit das untergeordnete Element in das übergeordnete Fenster gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec396-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="ec396-109">\_Durch die Angabe von CS-Parametern wird die Leistung einer Anwendung verbessert, da das System den sichtbaren Bereich nicht für jedes untergeordnete Fenster neu berechnen muss.</span><span class="sxs-lookup"><span data-stu-id="ec396-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="ec396-110">Vom übergeordneten Fenster festgelegte Attributwerte werden für das untergeordnete Fenster nicht beibehalten. Beispielsweise kann das übergeordnete Fenster den Pinsel nicht für seine untergeordneten Fenster festlegen.</span><span class="sxs-lookup"><span data-stu-id="ec396-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="ec396-111">Die einzige Eigenschaft, die beibehalten wird, ist der Clippingbereich.</span><span class="sxs-lookup"><span data-stu-id="ec396-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="ec396-112">Das Fenster muss seine eigene Ausgabe an die Begrenzungen des Fensters Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="ec396-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="ec396-113">Da der Clippingbereich für den übergeordneten Gerätekontext mit dem übergeordneten Fenster identisch ist, kann das untergeordnete Fenster potenziell über das gesamte übergeordnete Fenster zeichnen, aber der übergeordnete Gerätekontext darf nicht auf diese Weise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec396-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="ec396-114">Das System ignoriert den CS- \_ Parser-Stil, wenn das übergeordnete Fenster einen privaten oder einen Klassen Gerätekontext verwendet, wenn das übergeordnete Fenster seine untergeordneten Fenster schneidet oder wenn das untergeordnete Fenster seine untergeordneten Fenster oder gleich geordneten Fenster schneidet.</span><span class="sxs-lookup"><span data-stu-id="ec396-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



