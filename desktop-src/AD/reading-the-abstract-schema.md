---
title: Lesen des abstrakten Schemas
description: Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den attributeSchema-und classSchema-Objekten im Schema Container gespeichert sind.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Schema Active Directory, Lesen des abstrakten Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858123"
---
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="633bc-104">Lesen des abstrakten Schemas</span><span class="sxs-lookup"><span data-stu-id="633bc-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="633bc-105">Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den **attributeSchema** -und **classSchema** -Objekten im Schema Container gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="633bc-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="633bc-106">Zum Abrufen von Daten, die im abstrakten Schema nicht verfügbar sind, lesen Sie die Daten direkt aus dem Schema Container, wie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="633bc-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="633bc-107">Verwenden Sie die Bindungs Zeichenfolge "LDAP://Schema", um eine Bindung an einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Zeiger auf das abstrakte Schema herzustellen.</span><span class="sxs-lookup"><span data-stu-id="633bc-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="633bc-108">Verwenden Sie diesen Zeiger, um die Klassen-, Attribut-und Syntax Einträge im abstrakten Schema aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="633bc-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="633bc-109">Sie können auch die [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) -Methode verwenden, um einzelne Einträge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="633bc-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



<span data-ttu-id="633bc-110">Verwenden Sie eine ähnliche Bindungs Zeichenfolge ("LDAP://Schema/ <object> "), um direkt an einen Klassen-oder Attribut Eintrag im abstrakten Schema zu binden.</span><span class="sxs-lookup"><span data-stu-id="633bc-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="633bc-111">In dieser Zeichenfolge &lt; ist "Object &gt; " der **ldapDisplayName** einer Klasse oder eines Attributs.</span><span class="sxs-lookup"><span data-stu-id="633bc-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="633bc-112">Für Klassen, die an die [**iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) -Schnittstelle gebunden sind; Binden Sie für Attribute an die [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="633bc-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



<span data-ttu-id="633bc-113">Außerdem stellt die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle die [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="633bc-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="633bc-114">Diese Eigenschaft gibt den ADsPath für die Objektklasse im Format der abstrakten Schema Bindungs Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="633bc-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="633bc-115">Wenn Sie einen **IADs** -Zeiger auf ein Objekt haben, können Sie mithilfe des von **IADs. Schema** zurückgegebenen ADsPath eine Bindung an die zugehörige Klasse im abstrakten Schema herstellen.</span><span class="sxs-lookup"><span data-stu-id="633bc-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="633bc-116">In der folgenden Tabelle sind die Schlüsseleigenschaften aufgeführt, die vom abstrakten Schema bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="633bc-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="633bc-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="633bc-117">Property</span></span>                                                             | <span data-ttu-id="633bc-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="633bc-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="633bc-119">**Iadsclass. Abstract**</span><span class="sxs-lookup"><span data-stu-id="633bc-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="633bc-120">Gibt an, ob dies eine abstrakte Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="633bc-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="633bc-121">**Iadsclass. hilfskit**</span><span class="sxs-lookup"><span data-stu-id="633bc-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="633bc-122">Gibt an, ob es sich um eine Hilfsklasse handelt.</span><span class="sxs-lookup"><span data-stu-id="633bc-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="633bc-123">**Iadsclass. auxderivedfrom**</span><span class="sxs-lookup"><span data-stu-id="633bc-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="633bc-124">Array von Hilfsklassen, von denen diese Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="633bc-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="633bc-125">**Iadsclass. Container**</span><span class="sxs-lookup"><span data-stu-id="633bc-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="633bc-126">Gibt an, ob Objekte dieser Klasse andere-Objekte enthalten können, was true ist, wenn eine Klasse diese Klasse in der Liste der **possiblevorgesetzten** enthält.</span><span class="sxs-lookup"><span data-stu-id="633bc-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="633bc-127">**Iadsclass. derivedfrom**</span><span class="sxs-lookup"><span data-stu-id="633bc-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="633bc-128">Array von Klassen, von denen diese Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="633bc-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="633bc-129">**Iadsclass. MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="633bc-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="633bc-130">Ruft ein Array der obligatorischen Eigenschaften ab, die für eine Instanz der-Klasse festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="633bc-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="633bc-131">Die zurückgegebene Liste enthält alle Werte von **mustare** und **systemmustare** für die Klasse und die Klassen, von denen Sie abgeleitet wird, einschließlich übergeordneten Klassen und Hilfsklassen.</span><span class="sxs-lookup"><span data-stu-id="633bc-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="633bc-132">**Iadsclass. Oid**</span><span class="sxs-lookup"><span data-stu-id="633bc-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="633bc-133">Ruft die governsID der-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="633bc-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="633bc-134">**Iadsclass. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="633bc-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="633bc-135">Ruft ein Array der optionalen Eigenschaften ab, die möglicherweise für eine Instanz der-Klasse festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="633bc-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="633bc-136">Die zurückgegebene Liste enthält alle Werte für " **mayincludes** " und " **systemmayare** " für die Klasse und die Klassen, von denen Sie abgeleitet wird, einschließlich übergeordneten Klassen und Hilfsklassen.</span><span class="sxs-lookup"><span data-stu-id="633bc-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="633bc-137">**Iadsclass. possiblevorgesetzten**</span><span class="sxs-lookup"><span data-stu-id="633bc-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="633bc-138">Ruft ein Array der **possibledie** -Werte für die-Klasse ab, die die Objektklassen angibt, die Objekte dieser Klasse enthalten können.</span><span class="sxs-lookup"><span data-stu-id="633bc-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="633bc-139">Das abstrakte Schema ist im Schema Container im **unter Schema** Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="633bc-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="633bc-140">Um den Distinguished Name des **unter Schema** Objekts zu erhalten, binden Sie an RootDSE, und lesen Sie das **subschemasubentry** -Attribut, wie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="633bc-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="633bc-141">Beachten Sie, dass es effizienter ist, das abstrakte Schema durch Binden an "LDAP://Schema" zu lesen, als indem es direkt an das **unter Schema** Objekt gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="633bc-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 