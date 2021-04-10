---
description: ICE58 prüft, ob die Medien Tabelle nicht mehr als 80 Zeilen enthält.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960347"
---
# <a name="ice58"></a><span data-ttu-id="fbc95-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="fbc95-103">ICE58</span></span>

<span data-ttu-id="fbc95-104">ICE58 prüft, ob die [Medien Tabelle](media-table.md) nicht mehr als 80 Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="fbc95-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="fbc95-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="fbc95-105">Result</span></span>

<span data-ttu-id="fbc95-106">Von ICE58 gemeldete Warnungen bewirken, dass die Installation fehlschlägt, es sei denn, das Paket wird mit Windows Installer 2,0 oder höher installiert.</span><span class="sxs-lookup"><span data-stu-id="fbc95-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="fbc95-107">Ab Windows Installer 2,0 wird die Beschränkung auf mehr als 80 Medien Tabelleneinträge entfernt.</span><span class="sxs-lookup"><span data-stu-id="fbc95-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="fbc95-108">Es wird keine Warnung ausgegeben, wenn die [**Zusammenfassungs**](page-count-summary.md) Eigenschaft für die Seitenzählung des Pakets größer oder gleich 150 ist.</span><span class="sxs-lookup"><span data-stu-id="fbc95-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="fbc95-109">Pakete des Schemas 200 oder höher können nur von Windows Installer 2,0 oder höher installiert werden.</span><span class="sxs-lookup"><span data-stu-id="fbc95-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="fbc95-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fbc95-110">Example</span></span>

<span data-ttu-id="fbc95-111">ICE58 meldet die folgenden Fehler und Warnungen für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="fbc95-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="fbc95-112">Um diesen Fehler zu beheben, entfernen Sie nicht verwendete Medien Tabelleneinträge, konsolidieren Sie Medien Tabelleneinträge, die auf die gleichen Medien verweisen, und packen Sie die Anwendung neu, um das erforderliche Medium zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fbc95-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="fbc95-113">[Medien Tabelle](media-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="fbc95-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="fbc95-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="fbc95-114">DiskId</span></span> | <span data-ttu-id="fbc95-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="fbc95-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="fbc95-116">1</span><span class="sxs-lookup"><span data-stu-id="fbc95-116">1</span></span>      | <span data-ttu-id="fbc95-117">10</span><span class="sxs-lookup"><span data-stu-id="fbc95-117">10</span></span>             |
| <span data-ttu-id="fbc95-118">2</span><span class="sxs-lookup"><span data-stu-id="fbc95-118">2</span></span>      | <span data-ttu-id="fbc95-119">20</span><span class="sxs-lookup"><span data-stu-id="fbc95-119">20</span></span>             |
| <span data-ttu-id="fbc95-120">...</span><span class="sxs-lookup"><span data-stu-id="fbc95-120">...</span></span>    | <span data-ttu-id="fbc95-121">...</span><span class="sxs-lookup"><span data-stu-id="fbc95-121">...</span></span>            |
| <span data-ttu-id="fbc95-122">81</span><span class="sxs-lookup"><span data-stu-id="fbc95-122">81</span></span>     | <span data-ttu-id="fbc95-123">810</span><span class="sxs-lookup"><span data-stu-id="fbc95-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="fbc95-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbc95-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc95-125">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="fbc95-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



