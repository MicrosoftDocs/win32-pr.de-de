---
description: MTP-Erweiterungs Ereignisse
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: MTP-Erweiterungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373359"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="59a6b-103">MTP-Erweiterungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="59a6b-103">MTP Extension Events</span></span>

<span data-ttu-id="59a6b-104">Ereignisse benachrichtigen eine Anwendung, dass Änderungen am oder mit einem Gerät aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="59a6b-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="59a6b-105">Beispielsweise kann eine Anwendung registrieren, um Benachrichtigungen zu erhalten, dass ein Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="59a6b-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="59a6b-106">Vom Hersteller erweiterte Ereignis Codes</span><span class="sxs-lookup"><span data-stu-id="59a6b-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="59a6b-107">Wenn ein Gerätehersteller ein vom Hersteller erweitertes Ereignis unterstützt, kombiniert der Treiber den Ereignis Code des Anbieters (UInt16) mit den höchsten 16 Bits der GUID für die **\_ \_ \_ \_ Erweiterte \_ Ereignisse des WPD-Ereignis-MTP-Anbieters** .</span><span class="sxs-lookup"><span data-stu-id="59a6b-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="59a6b-108">Wenn beispielsweise der erweiterte Code des Anbieters 0xc001 ist, würde die resultierende GUID wie im folgenden Beispiel gezeigt lauten:</span><span class="sxs-lookup"><span data-stu-id="59a6b-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="59a6b-109">Vom Hersteller erweiterte Ereignis Parameter</span><span class="sxs-lookup"><span data-stu-id="59a6b-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="59a6b-110">Die Parameter für ein vom Hersteller erweitertes Ereignis werden von der Ereignis-ID-GUID des **WPD- \_ Ereignis \_ Parameters \_ \_** und der **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Ereignis \_** Parameter gemeldet, eine Auflistung von **propvarianten**.</span><span class="sxs-lookup"><span data-stu-id="59a6b-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="59a6b-111">Diese **propvarianten** entsprechen den Ereignis Parametern.</span><span class="sxs-lookup"><span data-stu-id="59a6b-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="59a6b-112">Wenn keine Parameter vorhanden sind, ist diese Auflistung leer.</span><span class="sxs-lookup"><span data-stu-id="59a6b-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="59a6b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59a6b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a6b-114">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="59a6b-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



