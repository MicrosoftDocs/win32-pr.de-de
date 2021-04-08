---
description: Die WMI-Skript Referenz enthält Definitionen für die WMI-Skript-API.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: Skript-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863799"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="6e7be-103">Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="6e7be-103">Scripting API for WMI</span></span>

<span data-ttu-id="6e7be-104">Die WMI-Skript Referenz enthält Definitionen für die WMI-Skript-API.</span><span class="sxs-lookup"><span data-stu-id="6e7be-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="6e7be-105">Verwenden Sie diese API, wenn Sie Anwendungen mit Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript) oder einer beliebigen anderen Skriptsprache schreiben, die Active Scripting-Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e7be-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="6e7be-106">PowerShell ist auch für die Skripterstellung mit WMI verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e7be-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="6e7be-107">Das Cmdlet "Get-WMI" und die drei typbeschleuniger ( \[ WMI \] , \[ WMIClass \] und \[ wmisearcher \] ) ermöglichen den grundlegenden administrativen Zugriff auf WMI.</span><span class="sxs-lookup"><span data-stu-id="6e7be-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="6e7be-108">Weitere Informationen finden Sie unter [Skripterstellung mit Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="6e7be-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="6e7be-109">WMI-Skript Objekte, mit Ausnahme von " [**Swap DateTime**](swbemdatetime.md) ", sind nicht als sichere Skripts für Skripts gekennzeichnet, die auf HTML-Seiten in Internet Explorer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6e7be-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="6e7be-110">Wenn die Sicherheitsstufe in Internet Explorer nicht gesenkt wird, schlägt das Skript fehl.</span><span class="sxs-lookup"><span data-stu-id="6e7be-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="6e7be-111">" **Taubemdatetime** " ist für die Initialisierung und Skripterstellung als sicher markiert.</span><span class="sxs-lookup"><span data-stu-id="6e7be-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="6e7be-112">Verwenden Sie allerdings alle WMI-Skript Objekte in **GetObject** -und **kreateobject** -aufrufen auf Server seitigem Code in Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="6e7be-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="6e7be-113">Skript-API-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="6e7be-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="6e7be-114">Dokument Konventionen für die Skript-API</span><span class="sxs-lookup"><span data-stu-id="6e7be-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="6e7be-115">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="6e7be-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="6e7be-116">Skript-API-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6e7be-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="6e7be-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e7be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e7be-118">WMI-Referenz</span><span class="sxs-lookup"><span data-stu-id="6e7be-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="6e7be-119">WMI-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="6e7be-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



