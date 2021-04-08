---
description: Wenn die transformssecure-Richtlinie auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort, an dem der Benutzer keinen Schreibzugriff hat, zwischengespeichert werden sollen.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Transformssecure-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861903"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="570ee-103">Transformssecure-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="570ee-103">TransformsSecure Policy</span></span>

<span data-ttu-id="570ee-104">Wenn die transformssecure-Richtlinie auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort, an dem der Benutzer keinen Schreibzugriff hat, zwischengespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="570ee-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="570ee-105">Das Festlegen dieser Richtlinie entspricht dem Festlegen der [transformssecure-Eigenschaft](transformssecure.md) , mit dem Unterschied, dass der Bereich anders ist.</span><span class="sxs-lookup"><span data-stu-id="570ee-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="570ee-106">Das Festlegen der transformssecure-Richtlinie gilt für alle Pakete, die auf einem bestimmten Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="570ee-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="570ee-107">Das Festlegen der transformssecure-Eigenschaft gilt unabhängig vom Computer für das Paket.</span><span class="sxs-lookup"><span data-stu-id="570ee-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="570ee-108">Der Zweck dieser Richtlinie besteht darin, einen sicheren Transformations Speicher mit Reisenden Benutzern von Windows 2000 bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="570ee-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="570ee-109">Ab Windows Server 2003 ist der Standardwert dieser Richtlinie 1.</span><span class="sxs-lookup"><span data-stu-id="570ee-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="570ee-110">Wenn diese Richtlinie festgelegt ist, kann bei einer [Wartungs Installation](maintenance-installation.md) nur die Transformation aus dem gesicherten Cache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="570ee-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="570ee-111">Wenn das Installationsprogramm feststellt, dass die Transformation auf dem lokalen Computer fehlt, versucht das Installationsprogramm, die Transformation wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="570ee-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="570ee-112">Damit das Installationsprogramm die Transformation wiederherstellen kann, muss sich die sichere Transformation in der Quell Liste des Installationspakets in einer autorisierten Quelle befinden.</span><span class="sxs-lookup"><span data-stu-id="570ee-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="570ee-113">Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="570ee-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="570ee-114">Die Wartungs Installation schlägt fehl, wenn die Transformation nicht verfügbar ist oder nicht geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="570ee-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="570ee-115">Wenn diese Richtlinie auf Windows Server 2003 nicht festgelegt ist, wird das Standardverhalten verwendet, um die Transformationen an einem sicheren Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="570ee-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="570ee-116">Wenn die Richtlinie in allen Versionen vor Windows Server 2003 nicht festgelegt ist, wird das Standardverhalten verwendet, um die Transformationen im Benutzerprofil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="570ee-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="570ee-117">Weitere Informationen finden Sie auch unter [gesicherte Transformationen](secured-transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="570ee-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="570ee-118">Windows Installer interpretiert die [transformsatsource-Richtlinie](transformsatsource-policy.md) so, dass Sie mit der transformssecure-Richtlinie identisch ist.</span><span class="sxs-lookup"><span data-stu-id="570ee-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="570ee-119">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="570ee-119">Registry Key</span></span>

<span data-ttu-id="570ee-120">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="570ee-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="570ee-121">Datentyp</span><span class="sxs-lookup"><span data-stu-id="570ee-121">Data Type</span></span>

<span data-ttu-id="570ee-122">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="570ee-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="570ee-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="570ee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="570ee-124">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="570ee-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



