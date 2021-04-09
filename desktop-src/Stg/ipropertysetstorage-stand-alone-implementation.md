---
title: IPropertySetStorage-eigenständige Implementierung
description: Die vom System bereitgestellte, eigenständige Implementierung von IPropertySetStorage enthält eine Implementierung von IPropertyStorage und IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage-Klasse,-Implementierungen,-Implementierungen
- IPropertySetStorage-Schnittstellen-STG, Implementierungen, eigenständige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039097"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="d098f-105">IPropertySetStorage-eigenständige Implementierung</span><span class="sxs-lookup"><span data-stu-id="d098f-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="d098f-106">Die vom System bereitgestellte, eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) enthält eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ist die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt.</span><span class="sxs-lookup"><span data-stu-id="d098f-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="d098f-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ist die Schnittstelle, mit der Eigenschafts Sätze in einem Speicher erstellt und geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d098f-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="d098f-108">Die Schnittstellen [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) und [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) werden auch in der eigenständigen Implementierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d098f-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="d098f-109">Um die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)zu verwenden, rufen Sie zunächst einen Zeiger auf die vom System bereitgestellte, eigenständige Implementierung ab, und ordnen Sie die vom System bereitgestellte Implementierung dem Speicher Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="d098f-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="d098f-110">Zum Abrufen eines Zeigers auf die eigenständige Implementierung von **IPropertySetStorage** müssen Sie die Funktion " [**stgkreatepropsetstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) " aufrufen und den *pstorage* -Parameter angeben, der das Speicher Objekt angibt, das den Eigenschaften Satz enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d098f-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="d098f-111">Diese Funktion stellt einen Zeiger auf die neue **IPropertySetStorage** -Schnittstelle für das angegebene Speicher Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="d098f-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="d098f-112">Die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) erstellt Eigenschafts Sätze für ein beliebiges Speicher Objekt, nicht nur für Verbund Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="d098f-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="d098f-113">Die eigenständige Implementierung ist nicht von Verbund Dateien abhängig und kann mit jeder Implementierung strukturierter Speicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d098f-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="d098f-114">Alle Einschränkungen der vom Aufrufer bereitgestellten strukturierten Speicher gelten für diese Implementierung von Eigenschaften Sätzen.</span><span class="sxs-lookup"><span data-stu-id="d098f-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="d098f-115">Wenn Sie z. b. einen Speicher im einfachen Modus für [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)bereitstellen, wird der resultierende **IPropertySetStorage** durch den bereitgestellten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="d098f-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="d098f-116">Weitere Informationen zur Implementierung der Verbund Datei dieser Schnittstelle finden Sie im Abschnitt [IPropertySetStorage-Verbund Datei Implementierung](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="d098f-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d098f-117">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="d098f-117">When to Use</span></span>

<span data-ttu-id="d098f-118">Rufen Sie die Methoden von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf, um Eigenschafts Sätze in strukturiertem Speicher zu erstellen, zu öffnen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d098f-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="d098f-119">Es gibt auch eine-Methode, die einen Zeiger auf den [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Enumerator bereitstellt, der zum Auflisten der Eigenschaften Sätze im Speicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d098f-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="d098f-120">Die eigenständige Implementierung stellt zusätzlich zu den Methoden " [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) " und " [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) " auch die Hilfsfunktionen " [**stgfoatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) " und " [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) " bereit, um Eigenschafts Sätze zu erstellen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d098f-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="d098f-121">Diese beiden Funktionen unterstützen den \_ nicht gepufferten Wert propsetflag, sodass Sie Änderungen direkt in den Eigenschaften Satz schreiben können, anstatt Sie in einem Cache zu puffern.</span><span class="sxs-lookup"><span data-stu-id="d098f-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="d098f-122">Weitere Informationen finden Sie unter [**propsetflag-Konstanten**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d098f-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="d098f-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="d098f-123">Methods</span></span>

<span data-ttu-id="d098f-124">Die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="d098f-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="d098f-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="d098f-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="d098f-126">Erstellt eine neue im Speicher festgelegte Eigenschaft und gibt einen Zeiger auf die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zurück.</span><span class="sxs-lookup"><span data-stu-id="d098f-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="d098f-127">Wenn Sie den nicht gepufferten Wert "propsetflag" verwenden möchten \_ , verwenden Sie stattdessen die Funktion " [**stgkreatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) ", um den neuen Eigenschaften Satz zu erstellen und zu öffnen und einen Zeiger auf die eigenständige Implementierung für die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d098f-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="d098f-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="d098f-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="d098f-129">Öffnet eine vorhandene im Speicher festgelegte Eigenschaft und gibt einen Zeiger auf die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zurück.</span><span class="sxs-lookup"><span data-stu-id="d098f-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="d098f-130">Wenn Sie den nicht gepufferten Wert "propsetflag" verwenden möchten \_ , verwenden Sie stattdessen die Funktion " [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) ", um einen Zeiger auf die eigenständige Implementierung von " [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) " für den angegebenen Eigenschaften Satz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d098f-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="d098f-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="d098f-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="d098f-132">Löscht eine Eigenschaft, die in diesem Eigenschaften Satz Speicher festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d098f-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="d098f-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="d098f-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="d098f-134">Erstellt ein-Objekt, das zum Auflisten von [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Wert-Strukturen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d098f-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="d098f-135">Jede **Status-setstg** -Struktur stellt Daten zu einem einzelnen Eigenschaften Satz bereit.</span><span class="sxs-lookup"><span data-stu-id="d098f-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="d098f-136">Die Eigenschaft "documentsummaryinformation" und "UserDefined" sind insofern eindeutig, als Sie möglicherweise zwei Eigenschaften Satz Abschnitte in einem einzelnen zugrunde liegenden Stream enthalten.</span><span class="sxs-lookup"><span data-stu-id="d098f-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="d098f-137">Weitere Informationen finden Sie in [den Eigenschaften Sätzen documentsummaryinformation und UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="d098f-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d098f-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d098f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d098f-139">IPropertyStorage-eigenständige Implementierung</span><span class="sxs-lookup"><span data-stu-id="d098f-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="d098f-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="d098f-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="d098f-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="d098f-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="d098f-142">**IStorage:: enumelements**</span><span class="sxs-lookup"><span data-stu-id="d098f-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="d098f-143">**Propsetflag-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="d098f-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="d098f-144">**Status-setstg**</span><span class="sxs-lookup"><span data-stu-id="d098f-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="d098f-145">**Stgkreatepropsetstg**</span><span class="sxs-lookup"><span data-stu-id="d098f-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="d098f-146">**Stgkreatepropstg**</span><span class="sxs-lookup"><span data-stu-id="d098f-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="d098f-147">**Stgopenpropstg**</span><span class="sxs-lookup"><span data-stu-id="d098f-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="d098f-148">**STGM-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="d098f-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 