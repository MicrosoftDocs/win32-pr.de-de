---
description: Die IWindowsDriverUpdate2-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: ed45a833-5c28-4ddc-993c-1237f69ec63f
title: IWindowsDriverUpdate2-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271e6623db073313c42a7e6dedebbd33e5eb6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526672"
---
# <a name="iwindowsdriverupdate2-properties"></a><span data-ttu-id="d2c7e-103">IWindowsDriverUpdate2-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2c7e-103">IWindowsDriverUpdate2 Properties</span></span>

<span data-ttu-id="d2c7e-104">Die [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-104">The [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="d2c7e-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2c7e-105">Property</span></span>                                                       | <span data-ttu-id="d2c7e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2c7e-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2c7e-107">**Cveids**</span><span class="sxs-lookup"><span data-stu-id="d2c7e-107">**CveIDs**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_cveids)                 | <span data-ttu-id="d2c7e-108">Enthält eine Sammlung der allgemeinen Bezeichner für Schwachstellen und exposures (CVE), die einem Update zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-108">Contains a collection of the Common Vulnerabilities and Exposures (CVE) identifiers that are associated with an update.</span></span> |
| [<span data-ttu-id="d2c7e-109">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="d2c7e-109">**IsPresent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_ispresent)           | <span data-ttu-id="d2c7e-110">Ruft einen booleschen Wert ab, der angibt, ob ein Update auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-110">Gets a Boolean value that indicates whether an update is installed on the computer.</span></span>                                     |
| [<span data-ttu-id="d2c7e-111">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="d2c7e-111">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_rebootrequired) | <span data-ttu-id="d2c7e-112">Ruft einen booleschen Wert ab, der angibt, ob der Computer nach der Installation oder Deinstallation eines Updates neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-112">Gets a Boolean value that indicates whether the computer must be restarted after you install or uninstall an update.</span></span>    |



 

<span data-ttu-id="d2c7e-113">Informationen zu den Membern, die von dieser Schnittstelle geerbt werden, finden Sie in der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-113">For information about the members inherited by this interface, see the following interface.</span></span>

-   [<span data-ttu-id="d2c7e-114">**Iwindowsdriverupdate**</span><span class="sxs-lookup"><span data-stu-id="d2c7e-114">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)

 

 



