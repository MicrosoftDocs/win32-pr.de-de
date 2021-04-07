---
title: Cenumschlag. CPP
description: In der Beispiel Anbieter Komponente verwendet die Enumeration eines Schema Objekts die Methoden aus "cenumsch. cpp", die in der folgenden Tabelle aufgeführt sind.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855344"
---
# <a name="cenumschcpp"></a><span data-ttu-id="2b111-103">Cenumschlag. CPP</span><span class="sxs-lookup"><span data-stu-id="2b111-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="2b111-104">In der Beispiel Anbieter Komponente verwendet die Enumeration eines Schema Objekts die Methoden aus "cenumsch. cpp", die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2b111-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="2b111-105">Methode</span><span class="sxs-lookup"><span data-stu-id="2b111-105">Method</span></span>                                        | <span data-ttu-id="2b111-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b111-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b111-107">**Csampledsschemaerum:: Create**</span><span class="sxs-lookup"><span data-stu-id="2b111-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="2b111-108">Erstellen Sie ein-Objekt, um die Enumeration eines ADSI-Schema Klassen Objekts zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="2b111-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="2b111-109">**Csampledsschemaerum:: csampledsschemaerum**</span><span class="sxs-lookup"><span data-stu-id="2b111-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="2b111-110">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="2b111-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="2b111-111">**Csampledsschemaerum:: ~ csampledsschemaerum**</span><span class="sxs-lookup"><span data-stu-id="2b111-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="2b111-112">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="2b111-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="2b111-113">**Csampledsschemaerum:: Next**</span><span class="sxs-lookup"><span data-stu-id="2b111-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="2b111-114">Ruft die angegebene Anzahl von Elementen aus dem angegebenen Schema Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="2b111-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="2b111-115">**Csampledsschemadenum:: umumubjects**</span><span class="sxs-lookup"><span data-stu-id="2b111-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="2b111-116">Verwaltet das Abrufen der Schnittstellen Zeiger auf die Objekte des Objekttyps, die angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2b111-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="2b111-117">**Csampledsschemadenum:: umumubjects**</span><span class="sxs-lookup"><span data-stu-id="2b111-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="2b111-118">Verwaltet das Abrufen der Schnittstellen Zeiger auf die Objekte des Standard Objekt Typs.</span><span class="sxs-lookup"><span data-stu-id="2b111-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="2b111-119">**Csampledsschemaenumum:: enumclasses**</span><span class="sxs-lookup"><span data-stu-id="2b111-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="2b111-120">Verwaltet das Abrufen der Schnittstellen Zeiger auf die in diesem-Objekt enthaltenen Schema Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="2b111-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="2b111-121">**Csampledsschemadenum:: GetClassObject**</span><span class="sxs-lookup"><span data-stu-id="2b111-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="2b111-122">Abrufen der nächsten Schema Klassendefinition Wenn Sie gefunden wird, erstellen Sie ein Schema Klassenobjekt, und geben Sie den Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="2b111-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="2b111-123">**Csampledsschemaenum:: EnumProperties**</span><span class="sxs-lookup"><span data-stu-id="2b111-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="2b111-124">Verwaltet das Abrufen der Schnittstellen Zeiger auf die Eigenschafts Objekte, die nur in diesem-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2b111-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="2b111-125">**Csampledsschemaenum:: getpropertyobject**</span><span class="sxs-lookup"><span data-stu-id="2b111-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="2b111-126">Abrufen der nächsten Eigenschafts Definition Wenn Sie gefunden wird, erstellen Sie ein Schema Klassenobjekt, und geben Sie den Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="2b111-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="2b111-127">**Csampledsschemaenumum:: enumsyntaxen**</span><span class="sxs-lookup"><span data-stu-id="2b111-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="2b111-128">Verwaltet das Abrufen der Schnittstellen Zeiger auf die Syntax Objekte, die nur in diesem-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2b111-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="2b111-129">**Csampledsschemaenum:: getsyntaxobject**</span><span class="sxs-lookup"><span data-stu-id="2b111-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="2b111-130">Abrufen der nächsten Syntax Definition Wenn Sie gefunden wird, erstellen Sie ein Schema Klassenobjekt, und geben Sie den Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="2b111-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




