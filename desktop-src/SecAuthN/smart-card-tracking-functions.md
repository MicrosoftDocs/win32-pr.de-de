---
description: Sie können Karten innerhalb von Lesern nachverfolgen. Diese Routinen verwenden in der Regel die Struktur "SCard \_ ReaderState" in einem Array.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Smartcard-nach Verfolgungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867456"
---
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="41b4f-104">Smartcard-nach Verfolgungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="41b4f-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="41b4f-105">Mit den folgenden Funktionen können Sie Karten innerhalb von Lesern nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="41b4f-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="41b4f-106">Diese Routinen verwenden in der Regel die Struktur " [**SCard \_ ReaderState**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) " in einem Array.</span><span class="sxs-lookup"><span data-stu-id="41b4f-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="41b4f-107">Thema</span><span class="sxs-lookup"><span data-stu-id="41b4f-107">Topic</span></span>                                                | <span data-ttu-id="41b4f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41b4f-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41b4f-109">**Scardlogecards**</span><span class="sxs-lookup"><span data-stu-id="41b4f-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="41b4f-110">Suchen Sie nach einer Karte, deren [*ATR-Zeichen*](../secgloss/a-gly.md) Folge mit einem angegebenen Kartennamen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="41b4f-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="41b4f-111">**ScardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="41b4f-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="41b4f-112">Blockiert die Ausführung, bis die aktuelle Verfügbarkeit von Karten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="41b4f-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="41b4f-113">**"SCardCancel"**</span><span class="sxs-lookup"><span data-stu-id="41b4f-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="41b4f-114">Beenden Sie ausstehende Aktionen.</span><span class="sxs-lookup"><span data-stu-id="41b4f-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
