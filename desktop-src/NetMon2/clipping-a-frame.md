---
description: Sie können angeben, dass der Treiber die Frames Ausschneiden soll.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Clipping eines Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351661"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="af1d3-103">Clipping eines Frames</span><span class="sxs-lookup"><span data-stu-id="af1d3-103">Clipping a Frame</span></span>

<span data-ttu-id="af1d3-104">Sie können angeben, dass der Treiber die Frames Ausschneiden soll.</span><span class="sxs-lookup"><span data-stu-id="af1d3-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="af1d3-105">(Wenn die anderen Erfassungs Filter Abschnitte ausgelassen werden, ist dies möglicherweise die einzige Funktion Ihres Erfassungs Filters).</span><span class="sxs-lookup"><span data-stu-id="af1d3-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="af1d3-106">Wenn das Feld **nframebytestocopy** nicht NULL (0) ist, gibt sein Wert an, wie viele Bytes jedes Frame erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="af1d3-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="af1d3-107">Wenn das Feld 0 (null) ist, wird der gesamte Frame beibehalten.</span><span class="sxs-lookup"><span data-stu-id="af1d3-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="af1d3-108">Sie können einen beliebigen Frame Ausschneiden, der die anderen Teile Ihres Erfassungs Filters durch Festlegen von **nframebytestocopy** übergibt.</span><span class="sxs-lookup"><span data-stu-id="af1d3-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



