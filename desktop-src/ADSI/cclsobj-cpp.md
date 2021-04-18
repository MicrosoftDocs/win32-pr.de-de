---
title: Cclsobj. CPP
description: In der Beispiel Anbieter Komponente sind die Funktionen für das Schema Klassenobjekt in cclsobj. cpp enthalten.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- Csampledsclass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340195"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="0386b-104">Cclsobj. CPP</span><span class="sxs-lookup"><span data-stu-id="0386b-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="0386b-105">In der Beispiel Anbieter Komponente sind die Funktionen für das Schema Klassenobjekt in cclsobj. cpp enthalten.</span><span class="sxs-lookup"><span data-stu-id="0386b-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="0386b-106">Die **csampledsclass** -Klasse ist in dieser Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="0386b-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="0386b-107">**Csampledsclass** ist mit Methoden und Eigenschaften definiert, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0386b-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="0386b-108">Methode</span><span class="sxs-lookup"><span data-stu-id="0386b-108">Method</span></span>                      | <span data-ttu-id="0386b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0386b-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0386b-110">**Csampledsclass**</span><span class="sxs-lookup"><span data-stu-id="0386b-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="0386b-111">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="0386b-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0386b-112">**~ Csampledsclass**</span><span class="sxs-lookup"><span data-stu-id="0386b-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="0386b-113">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="0386b-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="0386b-114">**"Feeclass"**</span><span class="sxs-lookup"><span data-stu-id="0386b-114">**CreateClass**</span></span>             | <span data-ttu-id="0386b-115">Erstellen Sie ein ADS-Schema Klassenobjekt.</span><span class="sxs-lookup"><span data-stu-id="0386b-115">Create an ADs schema class object.</span></span> <span data-ttu-id="0386b-116">Such Attribut Definitionen durch Aufrufen von **sampledsgetclassdefinition**.</span><span class="sxs-lookup"><span data-stu-id="0386b-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="0386b-117">**"Feeclass"**</span><span class="sxs-lookup"><span data-stu-id="0386b-117">**CreateClass**</span></span>             | <span data-ttu-id="0386b-118">Erstellen Sie ein Schema Klassenobjekt, wenn die Attribut Definitionen vorhanden sind, und legen Sie bekannte Attribute fest, wie z. b. die in [**iadsclass:: mandatoryattribute**](iadsclass-property-methods.md)aufgeführten.</span><span class="sxs-lookup"><span data-stu-id="0386b-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="0386b-119">**"Zugeordnete Zuordnung"**</span><span class="sxs-lookup"><span data-stu-id="0386b-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="0386b-120">Erstellen Sie ein Schema Klassenobjekt, und laden Sie dessen Typdaten.</span><span class="sxs-lookup"><span data-stu-id="0386b-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="0386b-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="0386b-121">**QueryInterface**</span></span>          | <span data-ttu-id="0386b-122">Gibt den angeforderten Schnittstellen Zeiger zurück, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0386b-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="0386b-123">Standard-IADs-Methoden.</span><span class="sxs-lookup"><span data-stu-id="0386b-123">Standard IADs methods.</span></span>      | <span data-ttu-id="0386b-124">Standard mäßige [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstellen Methoden, die in dieser Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0386b-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="0386b-125">Standard mäßige iadsclass-Methoden.</span><span class="sxs-lookup"><span data-stu-id="0386b-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="0386b-126">Standard mäßige [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstellen Methoden, die in dieser Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0386b-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="0386b-127">**"Kreatepropertylist"**</span><span class="sxs-lookup"><span data-stu-id="0386b-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="0386b-128">Erstellen Sie eine Liste von Eigenschaften, die dieser Schema Klasse zugeordnet sind, indem Sie **createpropertyentry** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0386b-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="0386b-129">**"Kreatepropertyentry"**</span><span class="sxs-lookup"><span data-stu-id="0386b-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="0386b-130">Erstellen Sie ein Eigenschafts Objekt in dieser Schema Klasse.</span><span class="sxs-lookup"><span data-stu-id="0386b-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="0386b-131">**Freipropertyentry**</span><span class="sxs-lookup"><span data-stu-id="0386b-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="0386b-132">Gibt den in " **kreatepropertyentry**" vorgenommenen Eintrag frei.</span><span class="sxs-lookup"><span data-stu-id="0386b-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="0386b-133">**Makevariantfromproplist**</span><span class="sxs-lookup"><span data-stu-id="0386b-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="0386b-134">Erstellen Sie ein Array von Varianten aus der von " **kreatepropertylist**" erstellten Eigenschaften Liste.</span><span class="sxs-lookup"><span data-stu-id="0386b-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="0386b-135">Kann in der Implementierung von [**iadsclass:: mandatoryattributs**](iadsclass-property-methods.md) usw. verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0386b-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




