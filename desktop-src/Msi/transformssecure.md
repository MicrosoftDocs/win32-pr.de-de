---
description: Wenn die transformssecure-Eigenschaft auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden, an dem der Benutzer keinen Schreibzugriff hat.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Transformssecure (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369266"
---
# <a name="transformssecure-property"></a><span data-ttu-id="e90da-103">Transformssecure (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e90da-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="e90da-104">Wenn die **transformssecure** -Eigenschaft auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden, an dem der Benutzer keinen Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="e90da-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="e90da-105">Das Festlegen dieser Eigenschaft entspricht dem Festlegen der [transformssecure-Richtlinie](transformssecure-policy.md) , mit der Ausnahme, dass der Bereich anders ist.</span><span class="sxs-lookup"><span data-stu-id="e90da-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="e90da-106">Das Festlegen der transformssecure-Richtlinie gilt für alle Pakete, die von einem bestimmten Benutzer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e90da-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="e90da-107">Das Festlegen der **transformssecure** -Eigenschaft gilt unabhängig vom Benutzer für das Paket.</span><span class="sxs-lookup"><span data-stu-id="e90da-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="e90da-108">Der Zweck dieser Eigenschaft ist die Bereitstellung von sicherem Transformations Speicher mit Reisenden Benutzern von Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e90da-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="e90da-109">Wenn diese Eigenschaft festgelegt ist, kann bei einer [Wartungs Installation](maintenance-installation.md) nur die Transformation aus dem angegebenen Pfad verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e90da-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="e90da-110">Wenn der Pfad nicht verfügbar ist, tritt bei der Wartungs Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e90da-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="e90da-111">Eine Quelle für jede sichere Transformation muss sich daher am Speicherort der Quelle des Installationspakets befinden.</span><span class="sxs-lookup"><span data-stu-id="e90da-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="e90da-112">Wenn das Installationsprogramm feststellt, dass die Transformation auf dem lokalen Computer fehlt, kann die Transformation aus dieser Quelle wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e90da-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="e90da-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e90da-113">Remarks</span></span>

<span data-ttu-id="e90da-114">Windows Installer interpretiert die [**transformsatsource**](transformsatsource.md) -Eigenschaft so, dass Sie mit der **transformssecure** -Eigenschaft identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e90da-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90da-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e90da-115">Requirements</span></span>



| <span data-ttu-id="e90da-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e90da-116">Requirement</span></span> | <span data-ttu-id="e90da-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e90da-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90da-118">Version</span><span class="sxs-lookup"><span data-stu-id="e90da-118">Version</span></span><br/> | <span data-ttu-id="e90da-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e90da-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e90da-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e90da-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e90da-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e90da-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e90da-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e90da-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e90da-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e90da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90da-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e90da-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e90da-125">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="e90da-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




