---
title: ADSI-Eigenschaften und-Attribute
description: Attribute werden manchmal auch als Eigenschaften bezeichnet. Dies kann Verwirrung verursachen. In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI-Eigenschaften und-Attribute ADSI
- ADSI ADSI, verwenden, zugreifen auf und Bearbeiten von Daten, Eigenschaften und Attributen
- Eigenschaften ADSI
- Attribute ADSI
- Eigenschaften ADSI, definiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338564"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="befa5-110">ADSI-Eigenschaften und-Attribute</span><span class="sxs-lookup"><span data-stu-id="befa5-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="befa5-111">Attribute werden manchmal auch als Eigenschaften bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="befa5-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="befa5-112">Dies kann Verwirrung verursachen.</span><span class="sxs-lookup"><span data-stu-id="befa5-112">This can cause confusion.</span></span> <span data-ttu-id="befa5-113">In dieser Dokumentation werden die folgenden Definitionen für Eigenschaften und Attribute verwendet.</span><span class="sxs-lookup"><span data-stu-id="befa5-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="befa5-114">Eigenschaften sind benannte Werte, die einem Programmier Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="befa5-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="befa5-115">Beispielsweise macht die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle Eigenschaften wie z. b. [**Klasse**](iads-property-methods.md) und **Name** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="befa5-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="befa5-116">Attribute sind die Daten, die Objekten in einem Verzeichnisdienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="befa5-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="befa5-117">Beispielsweise verfügt ein Benutzerobjekt über ein Attribut namens **CN** , das eine Zeichenfolge mit dem allgemeinen oder relativen Distinguished Name des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="befa5-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="befa5-118">Auf Attribute kann über Methoden der ADSI-Schnittstelle wie [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put)zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="befa5-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="befa5-119">Weitere Informationen zu Eigenschaften und Attributen von ADSI finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="befa5-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="befa5-120">Der ADSI-Attribut Cache</span><span class="sxs-lookup"><span data-stu-id="befa5-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="befa5-121">Einzelne Attribute und Attribute mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="befa5-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="befa5-122">Active Directory von Betriebs Attributen</span><span class="sxs-lookup"><span data-stu-id="befa5-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




