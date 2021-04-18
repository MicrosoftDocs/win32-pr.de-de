---
description: Das configurableitem-Objekt stellt eine einzelne Zeile aus der Tabelle ModuleConfiguration dar.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Configurableitem-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365782"
---
# <a name="configurableitem-object"></a><span data-ttu-id="f3cfd-103">Configurableitem-Objekt</span><span class="sxs-lookup"><span data-stu-id="f3cfd-103">ConfigurableItem object</span></span>

<span data-ttu-id="f3cfd-104">Das **configurableitem-Objekt** stellt eine einzelne Zeile aus der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)dar.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="f3cfd-105">Dabei handelt es sich um ein einzelnes konfigurierbares "Attribut" aus dem Modul.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="f3cfd-106">Die-Schnittstelle besteht aus schreibgeschützten Eigenschaften, eine für jede Spalte in der ModuleConfiguration-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="f3cfd-107">Die Schnittstellen Definition lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="f3cfd-108">Member</span><span class="sxs-lookup"><span data-stu-id="f3cfd-108">Members</span></span>

<span data-ttu-id="f3cfd-109">Das **configurableitem** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3cfd-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="f3cfd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3cfd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3cfd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3cfd-111">Properties</span></span>

<span data-ttu-id="f3cfd-112">Das **configurableitem** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="f3cfd-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3cfd-113">Property</span></span>                                                         | <span data-ttu-id="f3cfd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3cfd-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3cfd-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="f3cfd-116">Gibt den Wert im Feld Attribute des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="f3cfd-117">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="f3cfd-118">Gibt den Wert im Kontext Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="f3cfd-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="f3cfd-120">Gibt den Wert im DefaultValue-Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="f3cfd-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="f3cfd-122">Gibt den Wert im Beschreibungsfeld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="f3cfd-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="f3cfd-124">Gibt den Wert im Feld Display Name des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="f3cfd-125">**Ges**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="f3cfd-126">Gibt den Wert im Feld Format des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="f3cfd-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="f3cfd-128">Gibt den Wert im Feld HelpKeyword des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="f3cfd-129">**Helplocation**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="f3cfd-130">Gibt den Wert im Feld helplocation des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="f3cfd-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="f3cfd-132">Gibt den Wert im Feld Name des Datensatzes dieses Objekts in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="f3cfd-133">**type**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="f3cfd-134">Gibt den Wert im type-Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f3cfd-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="f3cfd-135">C++</span><span class="sxs-lookup"><span data-stu-id="f3cfd-135">C++</span></span>

<span data-ttu-id="f3cfd-136">Schnittstelle **imsmconfigurableitem: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="f3cfd-137">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="f3cfd-137">Interface ID</span></span>



| <span data-ttu-id="f3cfd-138">Konstante</span><span class="sxs-lookup"><span data-stu-id="f3cfd-138">Constant</span></span>                      | <span data-ttu-id="f3cfd-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f3cfd-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="f3cfd-140">**IID \_ imsmconfigurableitem**</span><span class="sxs-lookup"><span data-stu-id="f3cfd-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="f3cfd-141">{4d6e6284-d21d-401E-84b6-909e00b50f 71}</span><span class="sxs-lookup"><span data-stu-id="f3cfd-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f3cfd-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3cfd-142">Requirements</span></span>



| <span data-ttu-id="f3cfd-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3cfd-143">Requirement</span></span> | <span data-ttu-id="f3cfd-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f3cfd-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cfd-145">Version</span><span class="sxs-lookup"><span data-stu-id="f3cfd-145">Version</span></span><br/> | <span data-ttu-id="f3cfd-146">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3cfd-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="f3cfd-147">Header</span><span class="sxs-lookup"><span data-stu-id="f3cfd-147">Header</span></span><br/>  | <dl> <span data-ttu-id="f3cfd-148"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3cfd-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3cfd-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f3cfd-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3cfd-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3cfd-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




