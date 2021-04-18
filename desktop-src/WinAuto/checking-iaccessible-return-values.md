---
title: Überprüfen von IAccessible-Rückgabe Werten
description: Client Entwickler sollten sich nicht darauf verlassen, dass die Component Object Model (com)-Makros erfolgreich sind, und die IAccessible-Rückgabewerte konnten nicht getestet werden, da andere Werte als "S OK" als \_ erfolgreich angesehen werden.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338478"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="173d8-103">Überprüfen von IAccessible-Rückgabe Werten</span><span class="sxs-lookup"><span data-stu-id="173d8-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="173d8-104">Client Entwickler sollten sich nicht darauf verlassen, dass die Component Object Model (com) [**-Makros**](/windows/desktop/api/winerror/nf-winerror-failed) [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) sind, und die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Rückgabewerte konnten nicht getestet werden, da andere Werte als "S OK" als \_ erfolgreich angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="173d8-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="173d8-105">Eine Methode kann z. b. den Wert "false" zurückgeben \_ , was durch das Makro " **erfolgreich** " als erfolgreich angesehen wird, aber dennoch einen **null** -Zeiger in einem Output-Parameter erhält.</span><span class="sxs-lookup"><span data-stu-id="173d8-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="173d8-106">Client Entwickler müssen vor der Möglichkeit warnen, dass einige Server andere Fehlercodes als die dokumentierten Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="173d8-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="173d8-107">Um sicher zu sein, müssen Sie sicherstellen, dass alle Ausgabeparameter gültige Informationen enthalten und die folgenden Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="173d8-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="173d8-108">Alle Zeiger sind nicht **null**.</span><span class="sxs-lookup"><span data-stu-id="173d8-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="173d8-109">Der **VT** -Member einer beliebigen [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur ist nicht gleich VT \_ empty.</span><span class="sxs-lookup"><span data-stu-id="173d8-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 