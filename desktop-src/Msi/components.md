---
description: Das Component-Objekt stellt eine eindeutige Instanz einer Komponente dar, die für die Enumeration verfügbar ist.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Component-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351316"
---
# <a name="component-object"></a><span data-ttu-id="fec56-103">Component-Objekt</span><span class="sxs-lookup"><span data-stu-id="fec56-103">Component object</span></span>

<span data-ttu-id="fec56-104">Das Component-Objekt stellt eine eindeutige Instanz einer Komponente dar, die für die Enumeration verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fec56-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="fec56-105">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fec56-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="fec56-106">Dieses Objekt ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fec56-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="fec56-107">Member</span><span class="sxs-lookup"><span data-stu-id="fec56-107">Members</span></span>

<span data-ttu-id="fec56-108">Das **Komponenten** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fec56-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="fec56-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fec56-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fec56-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fec56-110">Properties</span></span>

<span data-ttu-id="fec56-111">Das **Komponenten** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fec56-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="fec56-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fec56-112">Property</span></span>                                                    | <span data-ttu-id="fec56-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fec56-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fec56-114">**Componentcode**</span><span class="sxs-lookup"><span data-stu-id="fec56-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="fec56-115">Der Komponenten Code der betreffenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="fec56-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="fec56-116">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="fec56-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="fec56-117">Der Kontext, der für die Anwendung auf die betreffende Komponente bestimmt wurde.</span><span class="sxs-lookup"><span data-stu-id="fec56-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="fec56-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="fec56-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="fec56-119">Die Benutzer-SID für die aufgelistete Komponente.</span><span class="sxs-lookup"><span data-stu-id="fec56-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="fec56-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fec56-120">Requirements</span></span>



| <span data-ttu-id="fec56-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fec56-121">Requirement</span></span> | <span data-ttu-id="fec56-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fec56-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fec56-123">Version</span><span class="sxs-lookup"><span data-stu-id="fec56-123">Version</span></span><br/> | <span data-ttu-id="fec56-124">Windows Installer 5,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fec56-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="fec56-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fec56-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fec56-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec56-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="fec56-127">IID</span><span class="sxs-lookup"><span data-stu-id="fec56-127">IID</span></span><br/>     | <span data-ttu-id="fec56-128">IID \_ IComponent ist definiert als 000c1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fec56-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="fec56-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fec56-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec56-130">Verwenden der Automatisierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="fec56-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="fec56-131">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fec56-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




