---
title: Fehler bei der Aria-Raster Struktur
description: Fehler bei der Aria-Raster Struktur
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- Ariagridstructureerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734593"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="130da-104">Fehler bei der Aria-Raster Struktur</span><span class="sxs-lookup"><span data-stu-id="130da-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="130da-105">Text</span><span class="sxs-lookup"><span data-stu-id="130da-105">Text</span></span>

<span data-ttu-id="130da-106">Das Element mit der **Raster** Rolle verfügt nicht über eine entsprechende Raster Struktur oder ein barrierefreies Markup.</span><span class="sxs-lookup"><span data-stu-id="130da-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="130da-107">type</span><span class="sxs-lookup"><span data-stu-id="130da-107">Type</span></span>

<span data-ttu-id="130da-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="130da-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="130da-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="130da-109">Description</span></span>

<span data-ttu-id="130da-110">Dieser Fehler gilt für benutzerdefinierte Elemente, für die das **Role** -Attribut auf "Grid" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="130da-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="130da-111">Es gilt nicht für HTML-Tabellen Tags, die die implizite **Rolle** "Grid" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="130da-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="130da-112">Für ein Element, für das das **Role** -Attribut auf "Grid" festgelegt ist, muss die Struktur definiert sein, die von der Web-Barrierefreiheits Initiative, auf die eine RIA-Aria-Raster Rolle zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="130da-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="130da-113">Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass Sie der Spezifikation "WAI-ARIA" entspricht.</span><span class="sxs-lookup"><span data-stu-id="130da-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="130da-114">Stellen Sie insbesondere sicher, dass die Struktur die folgenden Regeln erfüllt.</span><span class="sxs-lookup"><span data-stu-id="130da-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="130da-115">Das **Raster** enthält Zeilen-oder **Zeilen** **Gruppen** Elemente.</span><span class="sxs-lookup"><span data-stu-id="130da-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="130da-116">Zeilen **Gruppe** enthält **Zeilen** Elemente.</span><span class="sxs-lookup"><span data-stu-id="130da-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="130da-117">**Zeilen** Elemente enthalten **ColumnHeader** -oder **gridcell** -oder **RowHeader** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="130da-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="130da-118">Ein Barrierefreiheits Name sollte für **Raster**-, **ColumnHeader**-, **gridcell** -und **RowHeader** -Elemente mithilfe eines der folgenden Attribute definiert werden.</span><span class="sxs-lookup"><span data-stu-id="130da-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="130da-119">Das [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut für den Verweis auf das Element, das Text enthält.</span><span class="sxs-lookup"><span data-stu-id="130da-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="130da-120">das Attribut " [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) ", um den barrierefreien Namen direkt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="130da-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="130da-121">[**Titel**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) zum Erstellen einer QuickInfo, die zur gleichen Zeit als Name verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="130da-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




