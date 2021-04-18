---
description: 'Die Time-Eigenschaft ist die aktuelle Zeit in Stunden, Minuten und Sekunden als eine Zeichenfolge mit Literaltext im Format hh: mm: SS, wobei eine 24-Stunden-Uhrzeit verwendet wird.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Time-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371415"
---
# <a name="time-property"></a><span data-ttu-id="7b5cb-103">Time-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b5cb-103">Time property</span></span>

<span data-ttu-id="7b5cb-104">Die **time** -Eigenschaft ist die aktuelle Zeit in Stunden, Minuten und Sekunden als eine Zeichenfolge mit Literaltext im Format hh: mm: SS, wobei eine 24-Stunden-Uhrzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="7b5cb-105">Beispielsweise die Uhrzeit 6:57 Uhr</span><span class="sxs-lookup"><span data-stu-id="7b5cb-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="7b5cb-106">wird durch "18:57:00" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-106">is represented by "18:57:00".</span></span> <span data-ttu-id="7b5cb-107">Das Format des Werts hängt vom Gebiets Schema des Benutzers ab. es ist das Format, das mit der [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) -Funktion mit der \_ Option Time FORCE24HOURFORMAT \| time \_ notimemarker abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="7b5cb-108">Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paket Ersteller festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5cb-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b5cb-109">Remarks</span></span>

<span data-ttu-id="7b5cb-110">Da es sich hierbei um eine Text Zeichenfolge handelt, kann Sie nicht in bedingten Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5cb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b5cb-111">Requirements</span></span>



| <span data-ttu-id="7b5cb-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b5cb-112">Requirement</span></span> | <span data-ttu-id="7b5cb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7b5cb-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5cb-114">Version</span><span class="sxs-lookup"><span data-stu-id="7b5cb-114">Version</span></span><br/> | <span data-ttu-id="7b5cb-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b5cb-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b5cb-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b5cb-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7b5cb-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5cb-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b5cb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b5cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5cb-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b5cb-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
