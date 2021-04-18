---
description: Die Sources-Eigenschaft listet alle Quellen für die Patch-Instanz auf. Diese Eigenschaft ruft "msisourcelistenumschlag Sources" auf und gibt ein Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Patch. Sources (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357991"
---
# <a name="patchsources-property"></a><span data-ttu-id="fbf12-104">Patch. Sources (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fbf12-104">Patch.Sources property</span></span>

<span data-ttu-id="fbf12-105">Die **Sources** -Eigenschaft listet alle Quellen für die Patch-Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="fbf12-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="fbf12-106">Diese Eigenschaft ruft " [**msisourcelistenumschlag sources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) " auf und gibt ein Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fbf12-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="fbf12-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fbf12-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf12-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf12-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="fbf12-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fbf12-109">Property value</span></span>

<span data-ttu-id="fbf12-110">Der Typ der aufzuzählenden Quelle.</span><span class="sxs-lookup"><span data-stu-id="fbf12-110">The type of source to enumerate.</span></span> <span data-ttu-id="fbf12-111">Der Wert kann *msiinstallsourcetymessetwork* (1) oder *msiinstallsourcetypeurl* (2) sein.</span><span class="sxs-lookup"><span data-stu-id="fbf12-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf12-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf12-112">Requirements</span></span>



| <span data-ttu-id="fbf12-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf12-113">Requirement</span></span> | <span data-ttu-id="fbf12-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf12-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf12-115">Version</span><span class="sxs-lookup"><span data-stu-id="fbf12-115">Version</span></span><br/> | <span data-ttu-id="fbf12-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fbf12-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fbf12-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fbf12-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fbf12-118">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fbf12-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="fbf12-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf12-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="fbf12-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf12-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="fbf12-121">IID</span><span class="sxs-lookup"><span data-stu-id="fbf12-121">IID</span></span><br/>     | <span data-ttu-id="fbf12-122">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fbf12-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="fbf12-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf12-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf12-124">**Patch**</span><span class="sxs-lookup"><span data-stu-id="fbf12-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="fbf12-125">**Msisourcelistenumschlag Quellen**</span><span class="sxs-lookup"><span data-stu-id="fbf12-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="fbf12-126">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbf12-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




