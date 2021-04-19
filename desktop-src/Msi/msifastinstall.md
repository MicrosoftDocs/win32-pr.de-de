---
description: Die msifastinstall-Eigenschaft kann verwendet werden, um die Zeit zu verkürzen, die für die Installation eines großen Windows Installer Pakets erforderlich ist.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Msifastinstall (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366732"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="5262b-103">Msifastinstall (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5262b-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="5262b-104">Die **msifastinstall** -Eigenschaft kann verwendet werden, um die Zeit zu verkürzen, die für die Installation eines großen Windows Installer Pakets erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5262b-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="5262b-105">Die-Eigenschaft kann in der Befehlszeile oder in der [Eigenschaften](property-table.md) Tabelle festgelegt werden, um Vorgänge zu konfigurieren, die der Benutzer oder Entwickler für die Installation nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="5262b-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="5262b-106">Der Wert der **msifastinstall** -Eigenschaft kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="5262b-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="5262b-107">Wert</span><span class="sxs-lookup"><span data-stu-id="5262b-107">Value</span></span> | <span data-ttu-id="5262b-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5262b-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="5262b-109">0</span><span class="sxs-lookup"><span data-stu-id="5262b-109">0</span></span>     | <span data-ttu-id="5262b-110">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5262b-110">Default value</span></span>                                                                |
| <span data-ttu-id="5262b-111">1</span><span class="sxs-lookup"><span data-stu-id="5262b-111">1</span></span>     | <span data-ttu-id="5262b-112">Für diese Installation wurde kein Systemwiederherstellungspunkt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5262b-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="5262b-113">2</span><span class="sxs-lookup"><span data-stu-id="5262b-113">2</span></span>     | <span data-ttu-id="5262b-114">Führen Sie nur die [Datei Kosten](file-costing.md) aus, und überspringen Sie andere Kosten.</span><span class="sxs-lookup"><span data-stu-id="5262b-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="5262b-115">4</span><span class="sxs-lookup"><span data-stu-id="5262b-115">4</span></span>     | <span data-ttu-id="5262b-116">Reduzieren Sie die Häufigkeit von Statusmeldungen.</span><span class="sxs-lookup"><span data-stu-id="5262b-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="5262b-117">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5262b-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5262b-118">Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5262b-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5262b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5262b-119">Requirements</span></span>



| <span data-ttu-id="5262b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5262b-120">Requirement</span></span> | <span data-ttu-id="5262b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5262b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5262b-122">Version</span><span class="sxs-lookup"><span data-stu-id="5262b-122">Version</span></span><br/> | <span data-ttu-id="5262b-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5262b-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5262b-124">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5262b-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




