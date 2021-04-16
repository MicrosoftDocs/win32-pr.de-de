---
title: Schema Verwaltung
description: Die ADSI-Beispiel Anbieter Komponente definiert die Schema Klassen \ 0034; Organisationseinheit \ 0034; und \ 0034; Benutzer \ 0034; und verwaltet diese Schema Klassen auf folgende Weise.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Schema Verwaltung ADSI
- Schema Verwaltung ADSI
- Verwalten von Schemas ADSI
- Schemas, Verwalten von ADSI
- Verwalten eines Schema-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104556703"
---
# <a name="schema-management"></a><span data-ttu-id="6346d-108">Schema Verwaltung</span><span class="sxs-lookup"><span data-stu-id="6346d-108">Schema Management</span></span>

<span data-ttu-id="6346d-109">Die ADSI-Beispiel Anbieter Komponente definiert die Schema Klassen "Organisationseinheit" und "Benutzer" und verwaltet diese Schema Klassen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6346d-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="6346d-110">Die Schema Klasse "Organisationseinheit" wird durch ein ADS-Container Objekt dargestellt und kann andere "Organisationseinheiten" und "Benutzer" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6346d-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="6346d-111">Das Container Objekt unterstützt die Schnittstellen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)und [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="6346d-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="6346d-112">Die Schema Klasse "User" wird durch ein generisches Active Directory Objekt dargestellt und enthält keine anderen Typen von Objekten.</span><span class="sxs-lookup"><span data-stu-id="6346d-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="6346d-113">In der Beispiel Anbieter Komponente wird das User-Objekt als generisches Active Directory Objekt implementiert, das die Schnittstellen **IUnknown**, **IDispatch** und **IADs** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6346d-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="6346d-114">Beachten Sie, dass das Benutzerobjekt, in diesem Fall, die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6346d-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="6346d-115">Die Beispiel Anbieter Komponente muss auch das ADS-Namespace Objekt implementieren, das die Schnittstellen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)und [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6346d-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="6346d-116">In der folgenden Abbildung werden die Details des Schemas veranschaulicht, das die beiden Beispiel Schema Klassen für Anbieter Komponenten darstellt.</span><span class="sxs-lookup"><span data-stu-id="6346d-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![ADSI-Beispiel Anbieter-Komponenten Schema](images/dssmsch.png)

<span data-ttu-id="6346d-118">Beachten Sie, dass in der obigen Abbildung die Schema Klasse "Organisationseinheit" drei Eigenschaften definiert: "Description", "Headcounts" und "ID".</span><span class="sxs-lookup"><span data-stu-id="6346d-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="6346d-119">Die Schema Klasse "User" definiert vier Eigenschaften: "ID", "Name", "PhoneNumber" und "Title".</span><span class="sxs-lookup"><span data-stu-id="6346d-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="6346d-120">Die "ID"-Eigenschaft wird von beiden Schema Klassen gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="6346d-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="6346d-121">Jede Eigenschaft wird entweder durch das Zeichen "String" oder das "Integer"-Syntax Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="6346d-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="6346d-122">Syntax Objekte sind nicht in der ersten Version der Beispiel Anbieter Komponente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6346d-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="6346d-123">In den meisten Microsoft ADSI-Schema Implementierungen sind die Syntax Objekte jedoch im Schema Container Objekt enthalten, genauso wie die Schema Klasse und die Eigenschafts Objekte.</span><span class="sxs-lookup"><span data-stu-id="6346d-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="6346d-124">Aus diesem Grund werden Sie hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6346d-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="6346d-125">Diese Anbieter Komponente macht Schema Daten für die ADSI-Client Anwendung in Form von ADS-Klassen Objekten, ADS-Eigenschafts Objekten und ADS-Syntax Objekten verfügbar, sodass Schema Daten zur Laufzeit abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="6346d-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="6346d-126">Die für die Beispiel Anbieter Komponente definierten adspaths für die Schema Klassen-Containerobjekte sind "Sample://Seattle/Schema" und "Sample://Toronto/Schema".</span><span class="sxs-lookup"><span data-stu-id="6346d-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="6346d-127">In diesem Beispiel sind die Inhalte der Schemas identisch.</span><span class="sxs-lookup"><span data-stu-id="6346d-127">In this example, the contents of the schemas are identical.</span></span>

 

 