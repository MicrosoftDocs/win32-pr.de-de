---
description: Das FeatureInfo-Objekt enthält Informationen zur Zielfunktion und wird mithilfe der FeatureInfo-Methode aus dem Sitzungs Objekt erstellt.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: FeatureInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367425"
---
# <a name="featureinfo-object"></a><span data-ttu-id="78993-103">FeatureInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="78993-103">FeatureInfo object</span></span>

<span data-ttu-id="78993-104">Das **FeatureInfo** -Objekt enthält Informationen zur Zielfunktion und wird mithilfe der [**FeatureInfo**](session-featureinfo.md) -Methode aus dem [**Sitzungs**](session-object.md) Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="78993-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="78993-105">Member</span><span class="sxs-lookup"><span data-stu-id="78993-105">Members</span></span>

<span data-ttu-id="78993-106">Das **FeatureInfo** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="78993-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="78993-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78993-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78993-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78993-108">Properties</span></span>

<span data-ttu-id="78993-109">Das **FeatureInfo** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78993-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="78993-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="78993-110">Property</span></span>                                                  | <span data-ttu-id="78993-111">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="78993-111">Access type</span></span>           | <span data-ttu-id="78993-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78993-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78993-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="78993-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="78993-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78993-114">Read/write</span></span><br/> | <span data-ttu-id="78993-115">Gibt den Wert für die Funktion in der Spalte Attribute der Funktions Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="78993-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="78993-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78993-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="78993-117">Gibt die Beschreibung der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="78993-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="78993-118">**Titel**</span><span class="sxs-lookup"><span data-stu-id="78993-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="78993-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78993-119">Read-only</span></span><br/>  | <span data-ttu-id="78993-120">Gibt den Titel der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="78993-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="78993-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78993-121">Requirements</span></span>



| <span data-ttu-id="78993-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78993-122">Requirement</span></span> | <span data-ttu-id="78993-123">Wert</span><span class="sxs-lookup"><span data-stu-id="78993-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78993-124">Version</span><span class="sxs-lookup"><span data-stu-id="78993-124">Version</span></span><br/> | <span data-ttu-id="78993-125">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78993-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78993-126">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78993-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78993-127">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="78993-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="78993-128">DLL</span><span class="sxs-lookup"><span data-stu-id="78993-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="78993-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78993-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="78993-130">IID</span><span class="sxs-lookup"><span data-stu-id="78993-130">IID</span></span><br/>     | <span data-ttu-id="78993-131">IID \_ ifeatureinfo ist definiert als 000c109f-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="78993-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="78993-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78993-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78993-133">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="78993-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




