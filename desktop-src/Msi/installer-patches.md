---
description: Die Eigenschaft schreibgeschützte Patches des Installer-Objekts gibt ein stringlist-Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer. Patches (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370306"
---
# <a name="installerpatches-property"></a><span data-ttu-id="28ab1-103">Installer. Patches (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="28ab1-103">Installer.Patches property</span></span>

<span data-ttu-id="28ab1-104">Die Eigenschaft schreibgeschützte **Patches** des [**Installer**](installer-object.md) -Objekts gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.</span><span class="sxs-lookup"><span data-stu-id="28ab1-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="28ab1-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="28ab1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ab1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="28ab1-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="28ab1-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="28ab1-107">Property value</span></span>

<span data-ttu-id="28ab1-108">Gibt den Produktcode an.</span><span class="sxs-lookup"><span data-stu-id="28ab1-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ab1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28ab1-109">Remarks</span></span>

<span data-ttu-id="28ab1-110">Zum Auflisten der Patches durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="28ab1-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="28ab1-111">Da Patches nicht geordnet sind, weist jeder neue Patch einen beliebigen Index auf.</span><span class="sxs-lookup"><span data-stu-id="28ab1-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="28ab1-112">Dies bedeutet, dass die Funktion Patches in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="28ab1-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ab1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28ab1-113">Requirements</span></span>



| <span data-ttu-id="28ab1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28ab1-114">Requirement</span></span> | <span data-ttu-id="28ab1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="28ab1-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ab1-116">Version</span><span class="sxs-lookup"><span data-stu-id="28ab1-116">Version</span></span><br/> | <span data-ttu-id="28ab1-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28ab1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28ab1-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28ab1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28ab1-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="28ab1-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="28ab1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="28ab1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="28ab1-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28ab1-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="28ab1-122">IID</span><span class="sxs-lookup"><span data-stu-id="28ab1-122">IID</span></span><br/>     | <span data-ttu-id="28ab1-123">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="28ab1-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="28ab1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28ab1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ab1-125">**Msienumschlag**</span><span class="sxs-lookup"><span data-stu-id="28ab1-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




