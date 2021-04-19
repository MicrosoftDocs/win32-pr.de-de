---
description: Die Date-Eigenschaft entspricht dem aktuellen Monat, Tag und Jahr als Zeichenfolge mit Literaltext im Format mm/dd/yyyy.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359667"
---
# <a name="date-property"></a><span data-ttu-id="0caa2-103">Date-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0caa2-103">Date property</span></span>

<span data-ttu-id="0caa2-104">Die **Date** -Eigenschaft entspricht dem aktuellen Monat, Tag und Jahr als Zeichenfolge mit Literaltext im Format mm/dd/yyyy.</span><span class="sxs-lookup"><span data-stu-id="0caa2-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="0caa2-105">Beispielsweise kann das Datum 22. Juni 2005 als "06/22/2005" dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0caa2-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="0caa2-106">Das Format des Werts hängt vom Gebiets Schema des Benutzers ab. dabei handelt es sich um das Format, das mithilfe von [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) mit der \_ Option Datum SHORTDATE abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0caa2-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="0caa2-107">Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paket Ersteller festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0caa2-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="0caa2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0caa2-108">Remarks</span></span>

<span data-ttu-id="0caa2-109">Da es sich hierbei um eine Text Zeichenfolge handelt, kann Sie nicht in bedingten Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0caa2-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0caa2-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0caa2-110">Requirements</span></span>



| <span data-ttu-id="0caa2-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0caa2-111">Requirement</span></span> | <span data-ttu-id="0caa2-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0caa2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0caa2-113">Version</span><span class="sxs-lookup"><span data-stu-id="0caa2-113">Version</span></span><br/> | <span data-ttu-id="0caa2-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0caa2-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0caa2-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0caa2-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0caa2-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0caa2-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0caa2-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="0caa2-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0caa2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0caa2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0caa2-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0caa2-119">Properties</span></span>](properties.md)
</dt> </dl>

 

