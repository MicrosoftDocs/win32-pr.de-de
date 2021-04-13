---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an seine ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: Gerätekontext Funktionen ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978584"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="4fd12-103">Gerätekontext Funktionen ICM-Enabled</span><span class="sxs-lookup"><span data-stu-id="4fd12-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="4fd12-104">Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an seine ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="4fd12-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="4fd12-105">(Weitere Informationen finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span><span class="sxs-lookup"><span data-stu-id="4fd12-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="4fd12-106">Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fd12-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="4fd12-107">Die folgenden Gerätekontext Funktionen sind für die Verwendung mit ICM aktiviert:</span><span class="sxs-lookup"><span data-stu-id="4fd12-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="4fd12-108">**"Kreatecompatibledc"**</span><span class="sxs-lookup"><span data-stu-id="4fd12-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="4fd12-109">**-**</span><span class="sxs-lookup"><span data-stu-id="4fd12-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="4fd12-110">**Getdcbrushcolor**</span><span class="sxs-lookup"><span data-stu-id="4fd12-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="4fd12-111">**Getdcpcolor**</span><span class="sxs-lookup"><span data-stu-id="4fd12-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="4fd12-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="4fd12-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="4fd12-113">**SelectObject**</span><span class="sxs-lookup"><span data-stu-id="4fd12-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="4fd12-114">**Setdcbrushcolor**</span><span class="sxs-lookup"><span data-stu-id="4fd12-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="4fd12-115">**Setdcpcolor**</span><span class="sxs-lookup"><span data-stu-id="4fd12-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
