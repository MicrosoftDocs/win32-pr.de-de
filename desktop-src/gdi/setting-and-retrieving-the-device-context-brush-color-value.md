---
description: Im folgenden Beispiel wird gezeigt, wie eine Anwendung die aktuelle Domänen Controller Farbe mithilfe der Funktionen setdcbrushcolor und getdcbrushcolor abrufen kann.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Festlegen und Abrufen des Farbwerts für den Gerätekontext Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c684bfd50fd92959e9b8f7eac5baf96c62fd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994590"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a><span data-ttu-id="fb907-103">Festlegen und Abrufen des Farbwerts für den Gerätekontext Pinsel</span><span class="sxs-lookup"><span data-stu-id="fb907-103">Setting and Retrieving the Device Context Brush Color Value</span></span>

<span data-ttu-id="fb907-104">Im folgenden Beispiel wird gezeigt, wie eine Anwendung die aktuelle Domänen Controller Farbe mithilfe der Funktionen [**setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) und [**getdcbrushcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="fb907-104">The following example shows how an application can retrieve the current DC brush color by using the [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) and the [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) functions.</span></span>


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc, RGB(00,0xff;00);
PatBlt(0,0,200,200,PATCOPY)
SetDCBrushColor(hdc,RGB(00,00,0xff);
PatBlt(0,0,200,200,PATCOPY);
```



 

 



