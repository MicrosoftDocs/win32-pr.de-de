---
description: Ein Multitrack-Terminal kann als Terminal angesehen werden, das eine Sammlung anderer Terminals ist. Jedes untergeordnete Terminal (a &\# 0034; Track&\# 0034;) kann ein Multitrack-Terminal oder ein Single-Track-Terminal sein.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Informationen zu Multitrack-Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358883"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="d6df7-104">Informationen zu Multitrack-Terminals</span><span class="sxs-lookup"><span data-stu-id="d6df7-104">About Multitrack Terminals</span></span>

<span data-ttu-id="d6df7-105">Ein Multitrack-Terminal kann als Terminal angesehen werden, das eine Sammlung anderer Terminals ist.</span><span class="sxs-lookup"><span data-stu-id="d6df7-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="d6df7-106">Jedes untergeordnete Terminal ("Track") kann ein Multitrack-Terminal oder ein Single-Track-Terminal sein.</span><span class="sxs-lookup"><span data-stu-id="d6df7-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="d6df7-107">Alle Multitrack-Terminals machen die [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) -Schnittstelle verfügbar, die generische Methoden zum Aufzählen, erstellen und Entfernen von Nachverfolgung-Terminals von einem Multitrack-Terminal umfasst.</span><span class="sxs-lookup"><span data-stu-id="d6df7-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="d6df7-108">Alle Terminals, Single-Track und Multitrack, machen die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6df7-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="d6df7-109">Ein Client, der über einen Zeiger auf eine [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle verfügt, kann ermitteln, ob das Terminal Multitrack oder Single-Track ist, indem das Terminal nach der [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) -Schnittstelle abgefragt wird, die nur für Multitrack-Terminals verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d6df7-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="d6df7-110">Das übergeordnete Terminal verwendet möglicherweise die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle seiner Nachverfolgung-Terminals</span><span class="sxs-lookup"><span data-stu-id="d6df7-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="d6df7-111">Weitere Informationen finden Sie unter nach [Verfolgen von Terminals](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="d6df7-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
