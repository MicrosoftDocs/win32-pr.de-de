---
description: Wenn Sie die Eigenschaft arpnomodify festlegen, werden die Funktionen zum Hinzufügen oder Entfernen von Programmen in der Systemsteuerung deaktiviert, die das Produkt ändert.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Arpnomodify (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356480"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="10f7e-103">Arpnomodify (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="10f7e-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="10f7e-104">Wenn Sie die Eigenschaft **arpnomodify** festlegen, werden die Funktionen zum Hinzufügen oder Entfernen von Programmen in der Systemsteuerung deaktiviert, die das Produkt ändert.</span><span class="sxs-lookup"><span data-stu-id="10f7e-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="10f7e-105">Bei Windows 2000 wird die Schaltfläche **ändern** für das **Produkt in der** **Systemsteuerung** unter Software deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10f7e-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="10f7e-106">Unter älteren Betriebssystemen wird durch Klicken auf die Schaltfläche "Software **" das Produkt** deinstalliert, anstatt in den Wartungsmodus-Assistenten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="10f7e-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="10f7e-107">Wenn die **arpnomodify** -Eigenschaft festgelegt ist, schreibt die [registerproduct-Aktion](registerproduct-action.md) den Wert "nomodify" unter den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="10f7e-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="10f7e-108">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**</span><span class="sxs-lookup"><span data-stu-id="10f7e-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="10f7e-109">Wenn die **arpnomodify** -Eigenschaft festgelegt ist und die [**ARPNOREMOVE**](arpnoremove.md) -Eigenschaft nicht festgelegt ist, wird von der registerproduct-Aktion auch der UninstallString-Wert unter diesem Schlüssel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="10f7e-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="10f7e-110">Der unistallstring-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="10f7e-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f7e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10f7e-111">Remarks</span></span>

<span data-ttu-id="10f7e-112">Unter Windows 2000 wird dadurch die Schaltfläche **ändern** für das Produkt in den **Programmen** Software der **Systemsteuerung** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10f7e-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="10f7e-113">Diese Eigenschaft kann durch eine Anpassungs Transformation festgelegt werden, um zu verhindern, dass Benutzer die Anpassung eines **Administrators über "** Software" ändern.</span><span class="sxs-lookup"><span data-stu-id="10f7e-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="10f7e-114">Diese Eigenschaft wirkt sich nur auf die Option **Programme hinzufügen oder entfernen**.</span><span class="sxs-lookup"><span data-stu-id="10f7e-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f7e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f7e-115">Requirements</span></span>



| <span data-ttu-id="10f7e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10f7e-116">Requirement</span></span> | <span data-ttu-id="10f7e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10f7e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f7e-118">Version</span><span class="sxs-lookup"><span data-stu-id="10f7e-118">Version</span></span><br/> | <span data-ttu-id="10f7e-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10f7e-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="10f7e-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10f7e-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="10f7e-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10f7e-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="10f7e-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="10f7e-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10f7e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10f7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f7e-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10f7e-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="10f7e-125">Beispiel für eine Anpassungs Transformation</span><span class="sxs-lookup"><span data-stu-id="10f7e-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




