---
description: Die folgenden Definitionen stellen eine Reihe von streamzuständen dar, die für die abgeleitete Klasse nützlich sein können, obwohl ihre Verwendung nicht erforderlich ist. Abgeleitete Klassen können die Menge der verfügbaren Zustände mühelos erweitern, indem Sie einfach zusätzliche Werte definieren.
ms.assetid: 2c719828-904f-4469-ab3b-a331f009b9c3
title: Cmspstream-Typdefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5395227b2c95bddb6b4b7ef7df391b610bf20bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364217"
---
# <a name="cmspstream-type-definitions"></a><span data-ttu-id="3018f-104">Cmspstream-Typdefinitionen</span><span class="sxs-lookup"><span data-stu-id="3018f-104">CMSPStream Type Definitions</span></span>

<span data-ttu-id="3018f-105">Die folgenden Definitionen stellen eine Reihe von streamzuständen dar, die für die abgeleitete Klasse nützlich sein können, obwohl ihre Verwendung nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3018f-105">The following definitions provide a set of stream states that may be useful to the derived class, although their use is not required.</span></span> <span data-ttu-id="3018f-106">Abgeleitete Klassen können die Menge der verfügbaren Zustände mühelos erweitern, indem Sie einfach zusätzliche Werte definieren.</span><span class="sxs-lookup"><span data-stu-id="3018f-106">Derived classes can conveniently extend the set of available states simply by defining additional values.</span></span>

``` syntax
#define STRM_INITIAL            0x00000000
#define STRM_TERMINALSELECTED   0x00000001
#define STRM_CONFIGURED         0x00000002
#define STRM_RUNNING            0x00000004
#define STRM_PAUSED             0x00000008
#define STRM_STOPPED            0x00000010
```

## <a name="related-topics"></a><span data-ttu-id="3018f-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3018f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3018f-108">**Cmspstream**</span><span class="sxs-lookup"><span data-stu-id="3018f-108">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



