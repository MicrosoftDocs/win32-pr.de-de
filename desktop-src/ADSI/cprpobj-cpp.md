---
title: Cprpobj. CPP
description: In der Beispiel Anbieter Komponente sind die Eigenschaften Objektmethoden in cprpobj. cpp in der folgenden Tabelle aufgeführt.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206248"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="81f7d-103">Cprpobj. CPP</span><span class="sxs-lookup"><span data-stu-id="81f7d-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="81f7d-104">In der Beispiel Anbieter Komponente sind die Eigenschaften Objektmethoden in cprpobj. cpp in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="81f7d-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="81f7d-105">Methode</span><span class="sxs-lookup"><span data-stu-id="81f7d-105">Method</span></span>                                                 | <span data-ttu-id="81f7d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81f7d-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f7d-107">**Csampledsproperty:: csampledsproperty**</span><span class="sxs-lookup"><span data-stu-id="81f7d-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="81f7d-108">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="81f7d-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="81f7d-109">**Csampledsproperty:: ~ csampledsproperty**</span><span class="sxs-lookup"><span data-stu-id="81f7d-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="81f7d-110">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="81f7d-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="81f7d-111">**Csampledsproperty:: kreateproperty**</span><span class="sxs-lookup"><span data-stu-id="81f7d-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="81f7d-112">Erstellen Sie ein ADS-Eigenschafts Objekt, und suchen Sie nach den Attribut Definitionen, indem Sie **sampledsgetpropertydefinition** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="81f7d-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="81f7d-113">**Csampledsproperty:: kreateproperty**</span><span class="sxs-lookup"><span data-stu-id="81f7d-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="81f7d-114">Erstellen Sie bei der Attribut Definition ein Eigenschafts Objekt, und legen Sie die Entsprechung zwischen unterstützten ADS-Syntaxen und den Anbieter Syntaxen fest.</span><span class="sxs-lookup"><span data-stu-id="81f7d-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="81f7d-115">**Csampledsproperty:: Zuordnungs propertyobject**</span><span class="sxs-lookup"><span data-stu-id="81f7d-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="81f7d-116">Erstellen Sie ein Property-Objekt, und laden Sie dessen Typdaten.</span><span class="sxs-lookup"><span data-stu-id="81f7d-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="81f7d-117">**Csampledsproperty:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="81f7d-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="81f7d-118">Gibt den angeforderten Schnittstellen Zeiger zurück, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81f7d-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="81f7d-119">Standard- [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="81f7d-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="81f7d-120">Standard mäßige [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="81f7d-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="81f7d-121">**Mapsyntaxidesadssyntax**</span><span class="sxs-lookup"><span data-stu-id="81f7d-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="81f7d-122">Legen Sie die Übereinstimmung zwischen der Syntax-ID und der ADS-Syntax fest.</span><span class="sxs-lookup"><span data-stu-id="81f7d-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="81f7d-123">**Mapsyntaxidessampledssyntax**</span><span class="sxs-lookup"><span data-stu-id="81f7d-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="81f7d-124">Legen Sie die Übereinstimmung zwischen der Syntax-ID und der Anbieter Syntax fest.</span><span class="sxs-lookup"><span data-stu-id="81f7d-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




