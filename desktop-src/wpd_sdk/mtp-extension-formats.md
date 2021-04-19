---
description: MTP-Erweiterungs Formate
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP-Erweiterungs Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349928"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="ab079-103">MTP-Erweiterungs Formate</span><span class="sxs-lookup"><span data-stu-id="ab079-103">MTP Extension Formats</span></span>

<span data-ttu-id="ab079-104">Das Format einer Datei auf einem Gerät kann durch einen GUID-Wert beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ab079-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="ab079-105">Dieser Wert wird von der Eigenschaft WPD- \_ Objekt \_ Format angegeben.</span><span class="sxs-lookup"><span data-stu-id="ab079-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="ab079-106">Vom Hersteller erweiterte Formate</span><span class="sxs-lookup"><span data-stu-id="ab079-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="ab079-107">Wenn ein Gerätehersteller das vom Hersteller erweiterte Format unterstützt, kombiniert der Treiber den Format Code des Herstellers (UInt16) mit den höchsten 16 Bits des **\_ \_ \_ nicht spezifizierten GUID des WPD-Objekt Formats** .</span><span class="sxs-lookup"><span data-stu-id="ab079-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="ab079-108">Wenn beispielsweise der erweiterte Code des Anbieters 0xb001 ist, würde die resultierende GUID wie im folgenden Beispiel gezeigt lauten:</span><span class="sxs-lookup"><span data-stu-id="ab079-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="ab079-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab079-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab079-110">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ab079-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



