---
title: Tabbedbackunknownelement
description: Tabbedbackunknownelement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388156"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="cae42-103">Tabbedbackunknownelement</span><span class="sxs-lookup"><span data-stu-id="cae42-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="cae42-104">Text</span><span class="sxs-lookup"><span data-stu-id="cae42-104">Text</span></span>

<span data-ttu-id="cae42-105">Tabstopps ist an ein Element außerhalb des Ziel-HWND gegangen.</span><span class="sxs-lookup"><span data-stu-id="cae42-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="cae42-106">type</span><span class="sxs-lookup"><span data-stu-id="cae42-106">Type</span></span>

<span data-ttu-id="cae42-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="cae42-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="cae42-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cae42-108">Description</span></span>

<span data-ttu-id="cae42-109">Die Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) bewirkt, dass der Fokus außerhalb des HWND des Überprüfungs Ziels verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="cae42-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="cae42-110">Die Zugriffs Prüfung verschiebt die Elementstruktur in das HWND der obersten Ebene für das ausgewählte Überprüfungs Ziel, bevor Überprüfungs Tasks ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cae42-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="cae42-111">Dadurch wird die Anzahl falscher Fehler verringert, die generiert werden, wenn ein für die Überprüfung ausgewähltes HWND Teil eines komplexeren Client Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="cae42-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="cae42-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="cae42-112">Possible causes</span></span>

-   <span data-ttu-id="cae42-113">Das Überprüfungs Ziel erfordert keine Tabstopps-Implementierung, um vollständige Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cae42-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="cae42-114">Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="cae42-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




