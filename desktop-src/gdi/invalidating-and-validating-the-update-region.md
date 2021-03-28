---
description: Eine Anwendung erklärt einen Teil eines Fensters für ungültig und legt den Aktualisierungs Bereich mithilfe der invalidaterierten-oder InvalidateRgn-Funktion fest.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Ungültig machen und Validieren der Update Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978577"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="d02f1-103">Ungültig machen und Validieren der Update Region</span><span class="sxs-lookup"><span data-stu-id="d02f1-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="d02f1-104">Eine Anwendung erklärt einen Teil eines Fensters für ungültig und legt den Aktualisierungs Bereich mithilfe der [**invalidaterierten**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) -oder [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="d02f1-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="d02f1-105">Diese Funktionen fügen das angegebene Rechteck oder den Bereich (in den Client Koordinaten) dem Aktualisierungs Bereich hinzu, wobei das Rechteck oder die Region mit dem Element kombiniert wird, das vom System oder der Anwendung zuvor der Aktualisierungs Region hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d02f1-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="d02f1-106">Die [**invalidatup**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) -und [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktionen generieren keine [**WM- \_ Paint**](wm-paint.md) -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d02f1-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="d02f1-107">Stattdessen sammelt das System die Änderungen, die von diesen Funktionen vorgenommen werden, und ihre eigenen Änderungen, während ein Fenster andere Nachrichten in der Nachrichten Warteschlange verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d02f1-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="d02f1-108">Durch das Anhäufen von Änderungen werden alle Änderungen gleichzeitig von einem Fenster verarbeitet, statt Bits und Teile einzeln zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d02f1-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="d02f1-109">Die Funktionen [**validatenund**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validieren einen Teil des Fensters, indem ein angegebenes Rechteck oder eine angegebene Region aus dem Aktualisierungs Bereich entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f1-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="d02f1-110">Diese Funktionen werden in der Regel verwendet, wenn das Fenster vor dem Empfang der [**WM \_ Paint**](wm-paint.md) -Meldung einen bestimmten Teil des Bildschirms in der Update Region aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="d02f1-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 



