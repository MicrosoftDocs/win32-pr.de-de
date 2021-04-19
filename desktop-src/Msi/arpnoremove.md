---
description: Wenn Sie die Eigenschaft ARPNOREMOVE festlegen, wird die Funktion "Software" in der Systemsteuerung deaktiviert, mit der das Produkt entfernt wird.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361914"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="37add-103">ARPNOREMOVE (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37add-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="37add-104">Wenn **Sie** die Eigenschaft **ARPNOREMOVE** festlegen, wird die Funktion "Software" in der **Systemsteuerung** deaktiviert, mit der das Produkt entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="37add-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="37add-105">Bei Windows 2000 wird die Schaltfläche **Entfernen** für das **Produkt in der** **Systemsteuerung** unter Software deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="37add-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="37add-106">Bei früheren Betriebssystemen hat dies den Effekt, das Produkt aus der Liste der installierten Produkte in der Systemsteuerung **in der** **Systemsteuerung** zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="37add-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="37add-107">Wenn die **ARPNOREMOVE** -Eigenschaft festgelegt ist, schreibt die [registerproduct-Aktion](registerproduct-action.md) den Wert "NoRemove" unter den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="37add-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="37add-108">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**</span><span class="sxs-lookup"><span data-stu-id="37add-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="37add-109">Wenn Sie die **ARPNOREMOVE** -Eigenschaft festlegen, wird verhindert, dass der UninstallString-Wert unter diesem Schlüssel geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="37add-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="37add-110">Der unistallstring-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="37add-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="37add-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37add-111">Remarks</span></span>

<span data-ttu-id="37add-112">Diese Eigenschaft kann z. b. während einer Anpassungs Transformation festgelegt werden, um Benutzer daran zu hindern, eine Administrator Anpassung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="37add-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="37add-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37add-113">Requirements</span></span>



| <span data-ttu-id="37add-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37add-114">Requirement</span></span> | <span data-ttu-id="37add-115">Wert</span><span class="sxs-lookup"><span data-stu-id="37add-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37add-116">Version</span><span class="sxs-lookup"><span data-stu-id="37add-116">Version</span></span><br/> | <span data-ttu-id="37add-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37add-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="37add-118">Windows Installer 4,0 oder Windows Installer 4,5 oder höher unter Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37add-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="37add-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37add-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="37add-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="37add-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37add-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37add-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37add-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37add-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




