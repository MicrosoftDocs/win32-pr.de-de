---
description: Die ShortcutTarget-Eigenschaft des Installer-Objekts überprüft eine Verknüpfung und gibt, sofern verfügbar, das Produkt, den Funktionsnamen und die Komponente zurück.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer. ShortcutTarget-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370784"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="e13cc-103">Installer. ShortcutTarget-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e13cc-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="e13cc-104">Die **ShortcutTarget** -Eigenschaft des [**Installer**](installer-object.md) -Objekts überprüft eine Verknüpfung und gibt, sofern verfügbar, das Produkt, den Funktionsnamen und die Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="e13cc-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="e13cc-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e13cc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e13cc-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="e13cc-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e13cc-107">Property value</span></span>

<span data-ttu-id="e13cc-108">Vollständiger Pfad und Dateiname für die Datei.</span><span class="sxs-lookup"><span data-stu-id="e13cc-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13cc-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e13cc-109">Remarks</span></span>

<span data-ttu-id="e13cc-110">ShortcutTarget gibt ein [**Daten Satz Objekt**](record-object.md) zurück, das drei Felder enthält:</span><span class="sxs-lookup"><span data-stu-id="e13cc-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="e13cc-111">Field 1 ist eine GUID für den Produktcode der Verknüpfung, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e13cc-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="e13cc-112">Dieses Feld kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e13cc-112">This field can be null.</span></span>
-   <span data-ttu-id="e13cc-113">Feld 2 ist die Funktions-ID der Verknüpfung, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e13cc-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="e13cc-114">Dieses Feld kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e13cc-114">This field can be null.</span></span>
-   <span data-ttu-id="e13cc-115">Field 3 ist eine GUID für den Komponenten Code, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e13cc-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="e13cc-116">Dieses Feld kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e13cc-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13cc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e13cc-117">Requirements</span></span>



| <span data-ttu-id="e13cc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e13cc-118">Requirement</span></span> | <span data-ttu-id="e13cc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e13cc-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13cc-120">Version</span><span class="sxs-lookup"><span data-stu-id="e13cc-120">Version</span></span><br/> | <span data-ttu-id="e13cc-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e13cc-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e13cc-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e13cc-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e13cc-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e13cc-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e13cc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e13cc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e13cc-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13cc-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e13cc-126">IID</span><span class="sxs-lookup"><span data-stu-id="e13cc-126">IID</span></span><br/>     | <span data-ttu-id="e13cc-127">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e13cc-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e13cc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e13cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13cc-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="e13cc-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="e13cc-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="e13cc-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




