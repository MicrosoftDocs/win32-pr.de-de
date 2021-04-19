---
description: Wenn die limitui-Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Limitui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369400"
---
# <a name="limitui-property"></a><span data-ttu-id="c6a2a-103">Limitui (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6a2a-103">LIMITUI property</span></span>

<span data-ttu-id="c6a2a-104">Wenn die **limitui** -Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="c6a2a-105">Diese Eigenschaft ist in Paketen erforderlich, die über keine erstellte Benutzeroberfläche verfügen, aber trotzdem Benutzeroberflächen Tabellen wie die [Dialog Feld Tabelle](dialog-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="c6a2a-106">Eine Beschreibung der UI-Ebenen finden Sie unter [ **MsiSetInternalUI** .](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="c6a2a-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a2a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6a2a-107">Remarks</span></span>

<span data-ttu-id="c6a2a-108">Installationspakete, die die **limitui** -Eigenschaft enthalten, müssen auch die [**arpnomodify**](arpnomodify.md) -Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="c6a2a-109">Dies ist erforderlich, damit ein Benutzer das richtige Verhalten von der **System Steuerungs** Option "Software **" beim Versuch** , ein Produkt zu konfigurieren, erhält.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a2a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6a2a-110">Requirements</span></span>



| <span data-ttu-id="c6a2a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6a2a-111">Requirement</span></span> | <span data-ttu-id="c6a2a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c6a2a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a2a-113">Version</span><span class="sxs-lookup"><span data-stu-id="c6a2a-113">Version</span></span><br/> | <span data-ttu-id="c6a2a-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c6a2a-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c6a2a-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6a2a-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c6a2a-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a2a-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6a2a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6a2a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a2a-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6a2a-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c6a2a-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="c6a2a-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="c6a2a-121">**Arpnomodify**</span><span class="sxs-lookup"><span data-stu-id="c6a2a-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




