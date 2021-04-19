---
description: Legen Sie die msinodisablemedia-Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die disablemedia-Eigenschaft festlegt. Durch Festlegen der disablemedia-Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Msinodisablemedia (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361352"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="81894-104">Msinodisablemedia (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81894-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="81894-105">Legen Sie die **msinodisablemedia** -Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die [**disablemedia**](-disablemedia.md) -Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="81894-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="81894-106">Durch Festlegen der **disablemedia** -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.</span><span class="sxs-lookup"><span data-stu-id="81894-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="81894-107">Wenn **msinodisablemedia** nicht festgelegt ist, fügt das Installationsprogramm beim Ausführen einer [administrativen Installation](administrative-installation.md)möglicherweise [**disablemedia**](-disablemedia.md) zum Verwaltungs Eigenschaftenstream hinzu.</span><span class="sxs-lookup"><span data-stu-id="81894-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="81894-108">Dadurch wird verhindert, dass Benutzer, die aus dem administrativen Image installieren, von einem Medium installiert werden, z. b. CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="81894-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="81894-109">Beim Ausführen einer administrativen [**Installation fügt das**](-disablemedia.md) Installationsprogramm den Verwaltungs Eigenschaftenstream nur dann hinzu, wenn die Zusammenfassungs Eigenschaft der [**Seitenanzahl**](page-count-summary.md) kleiner als 150 ist.</span><span class="sxs-lookup"><span data-stu-id="81894-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="81894-110">Wenn [**disablemedia**](-disablemedia.md) in der Eigenschaft [**adminproperties**](adminproperties.md) aufgeführt ist, wird durch Festlegen von **msinodisablemedia** verhindert, dass **disablemedia** während einer administrativen Installation festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="81894-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="81894-111">In diesem Fall kann das Installationsprogramm eine Medienquelle registrieren, und ein Benutzer kann dann die Option zur erneuten Installation aus der Medienquelle auswählen, wenn das ursprüngliche administrative Installations Image später nicht mehr verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="81894-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="81894-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81894-112">Requirements</span></span>



| <span data-ttu-id="81894-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81894-113">Requirement</span></span> | <span data-ttu-id="81894-114">Wert</span><span class="sxs-lookup"><span data-stu-id="81894-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81894-115">Version</span><span class="sxs-lookup"><span data-stu-id="81894-115">Version</span></span><br/> | <span data-ttu-id="81894-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="81894-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="81894-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81894-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="81894-118">Windows Installer unter Windows Server 2003, Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="81894-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="81894-119">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="81894-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81894-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81894-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81894-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81894-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




