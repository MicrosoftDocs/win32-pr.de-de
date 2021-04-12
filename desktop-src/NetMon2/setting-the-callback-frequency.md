---
description: Verwenden Sie den folgenden Code, um die Rückruf Häufigkeit festzulegen.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Festlegen der Rückruf Häufigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343868"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="1f5a2-103">Festlegen der Rückruf Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="1f5a2-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="1f5a2-104">Verwenden Sie den folgenden Code, um die Rückruf Häufigkeit festzulegen:</span><span class="sxs-lookup"><span data-stu-id="1f5a2-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="1f5a2-105">**DWORD** Wert = 1;</span><span class="sxs-lookup"><span data-stu-id="1f5a2-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="1f5a2-106">Dieses Code Fragment legt die Rückruf Häufigkeit auf 1 Sekunde (Minimalwert) fest.</span><span class="sxs-lookup"><span data-stu-id="1f5a2-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="1f5a2-107">Der maximale Wert muss viel größer als 1 sein.</span><span class="sxs-lookup"><span data-stu-id="1f5a2-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="1f5a2-108">Wenn der NPP-Puffer (Network Packet Provider) voll ist, ruft der NPP den Monitor früher wieder auf.</span><span class="sxs-lookup"><span data-stu-id="1f5a2-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



