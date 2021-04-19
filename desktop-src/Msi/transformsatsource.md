---
description: Das Festlegen dieser Eigenschaft entspricht dem Festlegen der transformsatsource-Richtlinien Richtlinie, mit dem Unterschied, dass der Bereich abweicht.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Transformsatsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367824"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="86cdb-103">Transformsatsource (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="86cdb-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="86cdb-104">Das Festlegen dieser Eigenschaft entspricht dem Festlegen der [transformsatsource-Richtlinien](transformsatsource-policy.md) Richtlinie, mit dem Unterschied, dass der Bereich abweicht.</span><span class="sxs-lookup"><span data-stu-id="86cdb-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="86cdb-105">Das Festlegen der transformsatsource-Richtlinie gilt für alle Pakete, die von einem bestimmten Benutzer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="86cdb-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="86cdb-106">Das Festlegen der **transformsatsource** -Eigenschaft gilt unabhängig von den Benutzern für das Paket.</span><span class="sxs-lookup"><span data-stu-id="86cdb-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="86cdb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86cdb-107">Remarks</span></span>

<span data-ttu-id="86cdb-108">Windows Installer interpretiert die **transformsatsource** -Eigenschaft so, als handele es sich um die [**transformssecure**](transformssecure.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="86cdb-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="86cdb-109">Wenn das @-Flag in der [**Transformationen**](transforms.md) -Eigenschaft übermittelt wird, werden die Transformationen in der Liste von Windows Installer als [sichere Quell Transformationen](secure-at-source-transforms.md)behandelt.</span><span class="sxs-lookup"><span data-stu-id="86cdb-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86cdb-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86cdb-110">Requirements</span></span>



| <span data-ttu-id="86cdb-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86cdb-111">Requirement</span></span> | <span data-ttu-id="86cdb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="86cdb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cdb-113">Version</span><span class="sxs-lookup"><span data-stu-id="86cdb-113">Version</span></span><br/> | <span data-ttu-id="86cdb-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="86cdb-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="86cdb-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="86cdb-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="86cdb-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="86cdb-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="86cdb-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="86cdb-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86cdb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86cdb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cdb-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86cdb-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




