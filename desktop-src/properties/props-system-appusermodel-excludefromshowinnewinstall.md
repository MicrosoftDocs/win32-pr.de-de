---
description: Verhindert, dass ein Startmenü Eintrag für eine neu installierte Anwendungs Verknüpfung eine Hervorhebung empfängt.
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: System. appusermodel. excludefromshowinnetwinstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206cbbc6b07b0d3fec5833c046d4cb44c1e5e4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362495"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a><span data-ttu-id="0e167-103">System. appusermodel. excludefromshowinnetwinstall</span><span class="sxs-lookup"><span data-stu-id="0e167-103">System.AppUserModel.ExcludeFromShowInNewInstall</span></span>

<span data-ttu-id="0e167-104">Verhindert, dass ein Startmenü Eintrag für eine neu installierte Anwendungs **Verknüpfung eine hervor** Hebung empfängt.</span><span class="sxs-lookup"><span data-stu-id="0e167-104">Prevents a **Start** menu entry for a newly installed application shortcut from receiving a highlight.</span></span> <span data-ttu-id="0e167-105">Dies entspricht dem Löschen der Option **neu installierte Programme markieren** im Menü Fenster "Start" für ein einzelnes Element **Anpassen** .</span><span class="sxs-lookup"><span data-stu-id="0e167-105">This is equivalent to clearing the **Highlight newly installed programs** option in the **Customize Start Menu** window on an individual item.</span></span> <span data-ttu-id="0e167-106">Diese Eigenschaft sollte für Tastenkombinationen für Tools und sekundäre Anwendungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e167-106">This property should be set on shortcuts for tools and secondary applications.</span></span>

> [!Note]  
> <span data-ttu-id="0e167-107">Diese Eigenschaft ist Eigenschaft wird nur vom Startmenü unter Windows Vista und Windows 7 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e167-107">This property is property is only used by the Start menu on Windows Vista and Windows 7.</span></span> <span data-ttu-id="0e167-108">Die Eigenschaft wird nicht vom Startbildschirm oder Startmenü unter Windows 8 und höher verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e167-108">The property is not used by the Start screen or Start menu on Windows 8 and later</span></span>

 

<span data-ttu-id="0e167-109">.</span><span class="sxs-lookup"><span data-stu-id="0e167-109">.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="0e167-110">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e167-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="0e167-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e167-111">Remarks</span></span>

<span data-ttu-id="0e167-112">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0e167-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e167-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e167-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e167-114">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="0e167-114">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="0e167-115">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="0e167-115">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="0e167-116">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="0e167-116">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="0e167-117">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="0e167-117">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="0e167-118">propertydescription</span><span class="sxs-lookup"><span data-stu-id="0e167-118">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0e167-119">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="0e167-119">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-120">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="0e167-120">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-121">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="0e167-121">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-122">Display Info</span><span class="sxs-lookup"><span data-stu-id="0e167-122">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-123">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="0e167-123">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-124">StringFormat</span><span class="sxs-lookup"><span data-stu-id="0e167-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0e167-125">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="0e167-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0e167-126">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="0e167-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0e167-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0e167-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0e167-128">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="0e167-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0e167-129">enum</span><span class="sxs-lookup"><span data-stu-id="0e167-129">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="0e167-130">enumbereich</span><span class="sxs-lookup"><span data-stu-id="0e167-130">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="0e167-131">image</span><span class="sxs-lookup"><span data-stu-id="0e167-131">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="0e167-132">DrawControl</span><span class="sxs-lookup"><span data-stu-id="0e167-132">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e167-133">editcontrol</span><span class="sxs-lookup"><span data-stu-id="0e167-133">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e167-134">FilterControl</span><span class="sxs-lookup"><span data-stu-id="0e167-134">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0e167-135">querycontrol</span><span class="sxs-lookup"><span data-stu-id="0e167-135">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="0e167-136">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="0e167-136">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="0e167-137">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="0e167-137">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> <dt>

<span data-ttu-id="0e167-138">[startpinoption](/previous-versions//jj553605(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e167-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span></span>
</dt> </dl>

 

 
