---
description: Die Microsoft-erkenungen verwenden die folgenden GUIDs.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: Eigenschafts-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132028"
---
# <a name="property-guids"></a><span data-ttu-id="8afc6-103">Eigenschafts-GUIDs</span><span class="sxs-lookup"><span data-stu-id="8afc6-103">Property GUIDs</span></span>

<span data-ttu-id="8afc6-104">Die Microsoft-erkenungen verwenden die folgenden GUIDs.</span><span class="sxs-lookup"><span data-stu-id="8afc6-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="8afc6-105">Wenn möglich sollten diese GUIDs von Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8afc6-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="8afc6-106">Es wird jedoch erwartet und empfohlen, dass andere erkenungen zusätzliche GUIDs für Eigenschaften verwenden, die nicht von den Microsoft-erkenungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8afc6-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="8afc6-107">Alle Eigenschafts Funktionen wurden mit dem Verständnis entwickelt, dass die Liste der GUIDs von anderen Erkennungs Modulen erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8afc6-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="8afc6-108">Diese Eigenschafts Funktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8afc6-108">These property functions include:</span></span>

-   [<span data-ttu-id="8afc6-109">**Getcontextpropertylist-Funktion**</span><span class="sxs-lookup"><span data-stu-id="8afc6-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="8afc6-110">**Getcontextpropertyvalue-Funktion**</span><span class="sxs-lookup"><span data-stu-id="8afc6-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="8afc6-111">**Getresultpropertylist-Funktion**</span><span class="sxs-lookup"><span data-stu-id="8afc6-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="8afc6-112">**Setcontextpropertyvalue-Funktion**</span><span class="sxs-lookup"><span data-stu-id="8afc6-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="8afc6-113">In der folgenden Tabelle sind die in "msink AUT. h" (installiert in c: \\ Programme \\ Microsoft Tablet PC Platform SDK standardmäßig installierten Tablet PC-Eigenschafts-GUIDs \\ ) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8afc6-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="8afc6-114">GUID</span><span class="sxs-lookup"><span data-stu-id="8afc6-114">GUID</span></span>                                                  | <span data-ttu-id="8afc6-115">Definition</span><span class="sxs-lookup"><span data-stu-id="8afc6-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afc6-116">inkrecognitionproperty- \_ boxnumber</span><span class="sxs-lookup"><span data-stu-id="8afc6-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="8afc6-117">Der Index für die Alternative Box-Erkennung im Box-Modus</span><span class="sxs-lookup"><span data-stu-id="8afc6-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="8afc6-118">inkrecognitionproperty ( \_ LineNumber)</span><span class="sxs-lookup"><span data-stu-id="8afc6-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="8afc6-119">Die Zeilennummer</span><span class="sxs-lookup"><span data-stu-id="8afc6-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="8afc6-120">inkrecognitionproperty- \_ Segmentierung</span><span class="sxs-lookup"><span data-stu-id="8afc6-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="8afc6-121">Segmentierung von Wörtern und Zeichen durch die Erkennung</span><span class="sxs-lookup"><span data-stu-id="8afc6-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="8afc6-122">inkrecognitionproperty- \_ Hotpoint</span><span class="sxs-lookup"><span data-stu-id="8afc6-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="8afc6-123">Der heiß Punkt der Bewegung</span><span class="sxs-lookup"><span data-stu-id="8afc6-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="8afc6-124">inkrecognitionproperty \_ MaximumStrokeCount</span><span class="sxs-lookup"><span data-stu-id="8afc6-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="8afc6-125">Maximale Anzahl von Strichen für ein Segment</span><span class="sxs-lookup"><span data-stu-id="8afc6-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="8afc6-126">inkrecognitionproperty- \_ PointsPerInch</span><span class="sxs-lookup"><span data-stu-id="8afc6-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="8afc6-127">Die Metrik "Punkte pro Zoll"</span><span class="sxs-lookup"><span data-stu-id="8afc6-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="8afc6-128">inkrecognitionproperty \_ conficelevel</span><span class="sxs-lookup"><span data-stu-id="8afc6-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="8afc6-129">[**Vertrauen \_ Level**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="8afc6-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="8afc6-130">inkrecognitionproperty- \_ LineMetrics</span><span class="sxs-lookup"><span data-stu-id="8afc6-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="8afc6-131">Informationen zum Berechnen von Baseline, Mittelpunkt oder beidem, die im Gitter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8afc6-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




