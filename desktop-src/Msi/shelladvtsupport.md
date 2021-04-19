---
description: Die shelladvtsupport-Eigenschaft wird vom Installationsprogramm festgelegt, wenn die IShellLink-Schnittstelle des Systems die installerdeskriptorauflösung unterstützt.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Shelladvtsupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373583"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="04121-103">Shelladvtsupport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04121-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="04121-104">Die **shelladvtsupport** -Eigenschaft wird vom Installationsprogramm festgelegt, wenn die [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle des Systems die installerdeskriptorauflösung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04121-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="04121-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04121-105">Remarks</span></span>

<span data-ttu-id="04121-106">Wenn diese Eigenschaft festgelegt ist, unterstützt die [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle des Systems die installerdeskriptorauflösung.</span><span class="sxs-lookup"><span data-stu-id="04121-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="04121-107">Dies wird von Windows 2000 und Systemen unterstützt, die Internet Explorer 4,01 ausführen.</span><span class="sxs-lookup"><span data-stu-id="04121-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="04121-108">Wenn diese Eigenschaft nicht festgelegt ist, hat das Installationsprogramm das Standardverhalten, dass während der Installation nicht angekündigte Features erstellt werden, entweder lokal oder von der Quelle aus.</span><span class="sxs-lookup"><span data-stu-id="04121-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="04121-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04121-109">Requirements</span></span>



| <span data-ttu-id="04121-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04121-110">Requirement</span></span> | <span data-ttu-id="04121-111">Wert</span><span class="sxs-lookup"><span data-stu-id="04121-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04121-112">Version</span><span class="sxs-lookup"><span data-stu-id="04121-112">Version</span></span><br/> | <span data-ttu-id="04121-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="04121-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="04121-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04121-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="04121-115">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04121-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="04121-116">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="04121-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04121-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04121-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04121-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04121-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="04121-119">Platt Form Unterstützung für Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="04121-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
