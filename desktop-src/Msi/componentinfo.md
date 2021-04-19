---
description: Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen-Befehl von msigetcomponentpathex abgerufen werden kann.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: ComponentInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368529"
---
# <a name="componentinfo-object"></a><span data-ttu-id="d1541-103">ComponentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="d1541-103">ComponentInfo object</span></span>

<span data-ttu-id="d1541-104">Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen-Befehl von msigetcomponentpathex abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1541-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="d1541-105">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1541-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d1541-106">Dieses Objekt ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1541-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="d1541-107">Member</span><span class="sxs-lookup"><span data-stu-id="d1541-107">Members</span></span>

<span data-ttu-id="d1541-108">Das **ComponentInfo** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d1541-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="d1541-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1541-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1541-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1541-110">Properties</span></span>

<span data-ttu-id="d1541-111">Das **ComponentInfo** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1541-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="d1541-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d1541-112">Property</span></span>                                                        | <span data-ttu-id="d1541-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1541-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="d1541-114">**Componentcode**</span><span class="sxs-lookup"><span data-stu-id="d1541-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="d1541-115">Der Komponenten Code der betreffenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1541-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="d1541-116">**ADS**</span><span class="sxs-lookup"><span data-stu-id="d1541-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="d1541-117">Der Pfad der Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1541-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="d1541-118">**State**</span><span class="sxs-lookup"><span data-stu-id="d1541-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="d1541-119">Der Status der Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1541-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="d1541-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1541-120">Requirements</span></span>



| <span data-ttu-id="d1541-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1541-121">Requirement</span></span> | <span data-ttu-id="d1541-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d1541-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1541-123">Version</span><span class="sxs-lookup"><span data-stu-id="d1541-123">Version</span></span><br/> | <span data-ttu-id="d1541-124">Windows Installer 5,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d1541-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="d1541-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1541-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1541-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1541-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1541-127">IID</span><span class="sxs-lookup"><span data-stu-id="d1541-127">IID</span></span><br/>     | <span data-ttu-id="d1541-128">IID \_ icomponentinfo ist definiert als 000c1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d1541-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d1541-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1541-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1541-130">Verwenden der Automatisierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="d1541-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="d1541-131">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d1541-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




