---
description: Durch Festlegen der disablemedia-Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Disablemedia (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369521"
---
# <a name="disablemedia-property"></a><span data-ttu-id="3f026-104">Disablemedia (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3f026-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="3f026-105">Durch Festlegen der [**disablemedia**](disablemedia.md) -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.</span><span class="sxs-lookup"><span data-stu-id="3f026-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="3f026-106">Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="3f026-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f026-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f026-107">Remarks</span></span>

<span data-ttu-id="3f026-108">Beachten Sie, dass die [**disablemedia**](disablemedia.md) -Eigenschaft eine andere Auswirkung hat als das Festlegen der disablemedia-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="3f026-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="3f026-109">Durch das Festlegen von **disablemedia** wird die Registrierung einer Medienquelle verhindert. Dadurch wird auch die erstmalige Installation einer Anwendung aus den Medienquellen verhindert.</span><span class="sxs-lookup"><span data-stu-id="3f026-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="3f026-110">Ausführliche Informationen zum Sichern der Medienquellen der [*verwalteten Anwendung*](m-gly.md) für das Durchsuchen und installieren durch nicht Administratoren finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="3f026-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f026-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f026-111">Requirements</span></span>



| <span data-ttu-id="3f026-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f026-112">Requirement</span></span> | <span data-ttu-id="3f026-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3f026-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f026-114">Version</span><span class="sxs-lookup"><span data-stu-id="3f026-114">Version</span></span><br/> | <span data-ttu-id="3f026-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f026-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3f026-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3f026-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3f026-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f026-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3f026-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3f026-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f026-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f026-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f026-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f026-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




