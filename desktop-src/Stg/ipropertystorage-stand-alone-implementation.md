---
title: IPropertyStorage-eigenständige Implementierung
description: Die vom System bereitgestellte, eigenständige Implementierung von IPropertySetStorage enthält eine Implementierung von IPropertyStorage, die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-eigenständige Implementierung
- IPropertyStorage-Schnittstellen-STG, Implementierungen, eigenständige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390486"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="54ce3-105">IPropertyStorage-eigenständige Implementierung</span><span class="sxs-lookup"><span data-stu-id="54ce3-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="54ce3-106">Die vom System bereitgestellte, eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) enthält eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt.</span><span class="sxs-lookup"><span data-stu-id="54ce3-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="54ce3-107">Mit der **IPropertySetStorage** -Schnittstelle werden Eigenschafts Sätze in einem Speicher erstellt und geöffnet.</span><span class="sxs-lookup"><span data-stu-id="54ce3-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="54ce3-108">Die Schnittstellen [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) und [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) werden auch in der eigenständigen Implementierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="54ce3-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="54ce3-109">Rufen Sie zum Abrufen eines Zeigers auf die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)die [**stgfoatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) -Funktion auf, um einen neuen Eigenschaften Satz zu erstellen, oder [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , um den Schnittstellen Zeiger auf einen vorhandenen Eigenschaften Satz abzurufen (oder rufen Sie die [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -oder [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode der eigenständigen [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Implementierung auf).</span><span class="sxs-lookup"><span data-stu-id="54ce3-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="54ce3-110">Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) erstellt Eigenschafts Sätze für beliebige Speicher-oder Streamobjekte, nicht nur für zusammengesetzte Dateispeicher und Streams.</span><span class="sxs-lookup"><span data-stu-id="54ce3-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="54ce3-111">Die eigenständige Implementierung ist nicht von Verbund Dateien abhängig und kann mit jeder Implementierung strukturierter Speicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54ce3-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="54ce3-112">Weitere Informationen zur Implementierung der Verbund Datei dieser Schnittstelle finden Sie unter [IPropertyStorage-Verbund Datei Implementierung](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="54ce3-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="54ce3-113">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="54ce3-113">When to Use</span></span>

<span data-ttu-id="54ce3-114">Verwenden Sie [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , um Eigenschaften innerhalb eines einzelnen Eigenschaften Satzes zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="54ce3-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="54ce3-115">Die Methoden unterstützen das Lesen, schreiben und Löschen von Eigenschaften und den optionalen Zeichen folgen Namen, die Eigenschaften-IDs zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="54ce3-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="54ce3-116">Andere Methoden unterstützen die standardcommit-und Wiederherstellungs Speichervorgänge.</span><span class="sxs-lookup"><span data-stu-id="54ce3-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="54ce3-117">Es gibt auch eine-Methode, die die dem Eigenschaften Speicher zugeordneten Zeiten festlegt, und einen anderen, der die Zuweisung einer CLSID ermöglicht, um anderen Code, z. b. Benutzeroberflächen Code, mit dem Eigenschaften Satz zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="54ce3-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="54ce3-118">Die [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) -Methode stellt einen Zeiger auf die eigenständige Implementierung von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)zur Verfügung, die die Eigenschaften im Satz auflistet.</span><span class="sxs-lookup"><span data-stu-id="54ce3-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="54ce3-119">Eigenschaften Satz Formate Version 0 und Version 1</span><span class="sxs-lookup"><span data-stu-id="54ce3-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="54ce3-120">Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt sowohl Version 0 als auch die Eigenschaften Satz-Serialisierungsformate der Version 1.</span><span class="sxs-lookup"><span data-stu-id="54ce3-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="54ce3-121">Weitere Informationen finden Sie unter [Eigenschaften Satz-Serialisierung](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="54ce3-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="54ce3-122">Eigenschafts Sätze werden im Format Version 0 erstellt und bleiben in diesem Format, es sei denn, es werden neue Funktionen angefordert.</span><span class="sxs-lookup"><span data-stu-id="54ce3-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="54ce3-123">Zu diesem Zeitpunkt wird das Format auf Version 1 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="54ce3-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="54ce3-124">Wenn z. b. ein Eigenschaften Satz mit dem Standardflag propsetflag erstellt wird \_ , ist sein Format Version 0.</span><span class="sxs-lookup"><span data-stu-id="54ce3-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="54ce3-125">Solange die Eigenschaften Typen, die dem Format Version 0 entsprechen, in diesen Eigenschaften Satz geschrieben und daraus gelesen werden, verbleibt der Eigenschaften Satz im Format Version 0.</span><span class="sxs-lookup"><span data-stu-id="54ce3-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="54ce3-126">Wenn ein Eigenschaftentyp der Version 1 in den Eigenschaften Satz geschrieben wird, wird der Eigenschaften Satz automatisch auf Version 1 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="54ce3-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="54ce3-127">Anschließend kann dieser Eigenschaften Satz nicht mehr von Implementierungen gelesen werden, die nur Version 0 verstehen.</span><span class="sxs-lookup"><span data-stu-id="54ce3-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="54ce3-128">IPropertyStorage-und Variant-Typen</span><span class="sxs-lookup"><span data-stu-id="54ce3-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="54ce3-129">Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt nicht die Variant-Typen VT \_ unknown oder VT \_ Dispatch im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="54ce3-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="54ce3-130">Die folgenden Variant-Typen werden in einem SafeArray unterstützt. Das heißt, diese Werte können mit dem VT- \_ Array im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="54ce3-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="54ce3-131">In SAFEARRAY Unterstützte Variant-Typen durch die Implementierung der Verbund Datei von [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="54ce3-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="54ce3-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="54ce3-132">VT\_I1</span></span>

<span data-ttu-id="54ce3-133">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="54ce3-133">VT\_UI1</span></span>

<span data-ttu-id="54ce3-134">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="54ce3-134">VT\_I2</span></span>

<span data-ttu-id="54ce3-135">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="54ce3-135">VT\_UI2</span></span>

<span data-ttu-id="54ce3-136">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="54ce3-136">VT\_I4</span></span>

<span data-ttu-id="54ce3-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="54ce3-137">VT\_UI4</span></span>

<span data-ttu-id="54ce3-138">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="54ce3-138">VT\_INT</span></span>

<span data-ttu-id="54ce3-139">VT \_ uint</span><span class="sxs-lookup"><span data-stu-id="54ce3-139">VT\_UINT</span></span>

<span data-ttu-id="54ce3-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="54ce3-140">VT\_R4</span></span>

<span data-ttu-id="54ce3-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="54ce3-141">VT\_R8</span></span>

<span data-ttu-id="54ce3-142">VT- \_ CY</span><span class="sxs-lookup"><span data-stu-id="54ce3-142">VT\_CY</span></span>

<span data-ttu-id="54ce3-143">VT- \_ Datum</span><span class="sxs-lookup"><span data-stu-id="54ce3-143">VT\_DATE</span></span>

<span data-ttu-id="54ce3-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="54ce3-144">VT\_BSTR</span></span>

<span data-ttu-id="54ce3-145">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="54ce3-145">VT\_BOOL</span></span>

<span data-ttu-id="54ce3-146">VT ( \_ dezimal)</span><span class="sxs-lookup"><span data-stu-id="54ce3-146">VT\_DECIMAL</span></span>

<span data-ttu-id="54ce3-147">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="54ce3-147">VT\_ERROR</span></span>

<span data-ttu-id="54ce3-148">VT- \_ Variante</span><span class="sxs-lookup"><span data-stu-id="54ce3-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="54ce3-149">Wenn die VT- \_ Variante mit dem VT-Array kombiniert wird \_ , enthält das SAFEARRAY selbst [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="54ce3-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="54ce3-150">Allerdings müssen die Typen dieser Elemente aus der vorangehenden Liste entnommen werden, können nicht als VT \_ -Variant verwendet werden und dürfen keine VT- \_ Vektor-, VT \_ Array-oder VT- \_ ByRef-Indikatoren enthalten.</span><span class="sxs-lookup"><span data-stu-id="54ce3-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="54ce3-151">IPropertyStorage-Methoden</span><span class="sxs-lookup"><span data-stu-id="54ce3-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="54ce3-152">Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="54ce3-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="54ce3-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="54ce3-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-154">Liest die im *rgpspec* -Array angegebenen Eigenschaften und gibt die Werte aller gültigen Eigenschaften im *rgvar* -Array von [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="54ce3-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="54ce3-155">In der vom System bereitgestellten eigenständigen Implementierung führen doppelte Eigenschaften Bezeichner, die auf Stream-oder Speichertypen verweisen, zu mehreren Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , und der Erfolg oder Misserfolg von "read [**Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) " hängt von der zugrunde liegenden Speicher Implementierung der Freigabe offener Storages ab.</span><span class="sxs-lookup"><span data-stu-id="54ce3-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="54ce3-156">Um einen Thread sicheren Vorgang sicherzustellen, wenn dieselbe Stream-oder Speicher Wert Eigenschaft mehrmals durch denselben [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Zeiger angefordert wird, wird der offene Vorgang in Abhängigkeit davon, ob die Eigenschaft bereits geöffnet ist oder nicht, unabhängig davon, ob das zugrunde liegende Dateisystem mehrere Starts eines Streams oder Speichers verarbeitet, erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54ce3-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="54ce3-157">Folglich führt der Read [**Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) -Vorgang für eine Stream-oder Speicher Wert Eigenschaft immer zum Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), wobei der Zugriff (z. b. STGM \_ -Lese schreiben) und die Freigabe Werte (z. b. STGM- \_ Freigabe \_ exklusiv) angegeben werden, wenn der Eigenschafts Satz ursprünglich geöffnet oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="54ce3-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="54ce3-158">Wenn die Methode fehlschlägt, sind die in *rgvar* geschriebenen Werte nicht \[ \] definiert.</span><span class="sxs-lookup"><span data-stu-id="54ce3-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="54ce3-159">Wenn einige Stream-oder Speicher Wert Eigenschaften erfolgreich geöffnet werden, aber vor dem Abschluss der Ausführung ein Fehler auftritt, sollten diese Eigenschaften vor der Rückgabe der Methode freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54ce3-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: Write Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="54ce3-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-161">Schreibt die im *rgpspec* \[ \] -Array angegebenen Eigenschaften und weist Ihnen die in *rgvar* angegebenen [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Tags und-Werte zu \[ \] .</span><span class="sxs-lookup"><span data-stu-id="54ce3-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="54ce3-162">Eigenschaften, die bereits vorhanden sind, werden die angegebenen **PROPVARIANT** -Werte zugewiesen, und Eigenschaften, die derzeit nicht vorhanden sind, werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="54ce3-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eletemultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="54ce3-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-164">Löscht die in der *rgpspec* angegebenen Eigenschaften \[ \] .</span><span class="sxs-lookup"><span data-stu-id="54ce3-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage:: Read PropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="54ce3-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-166">Liest vorhandene Zeichen folgen Namen, die den im *rgpropid* -Array angegebenen Eigenschaften-IDs zugeordnet sind \[ \] .</span><span class="sxs-lookup"><span data-stu-id="54ce3-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage:: Beschreib tepropertynames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="54ce3-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-168">Weist den im *rgpropid* -Array angegebenen Eigenschaften-IDs Zeichen folgen Namen zu, die im *rglpwstrinname* -Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="54ce3-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletepropertynames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="54ce3-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-170">Löscht die Zeichen folgen Namen der Eigenschaften-IDs, die im *rgpropid* -Array angegeben sind, indem **null** in den Eigenschaftsnamen geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="54ce3-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: setClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="54ce3-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-172">Legt die **CLSID** des Eigenschaften Satz-Streams fest.</span><span class="sxs-lookup"><span data-stu-id="54ce3-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="54ce3-173">In der eigenständigen Implementierung wird durch das Festlegen der CLSID für einen nicht einfachen Eigenschaften Satz (einer, der Speicher-oder streamwerteigenschaften enthalten kann, wie in [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)beschrieben, auch die CLSID für den zugrunde liegenden unter Speicher festgelegt, sodass Sie durch einen Aufrufen von [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="54ce3-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="54ce3-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-175">Bei einfachen und nicht einfachen Eigenschafts Sätzen leert das Speicher Image in das Datenträger Subsystem.</span><span class="sxs-lookup"><span data-stu-id="54ce3-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="54ce3-176">Außerdem ruft diese Methode für nicht einfache Eigenschaften Sätze im Transaktionsmodus [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) für den Eigenschaften Satz auf.</span><span class="sxs-lookup"><span data-stu-id="54ce3-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="54ce3-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-178">Nur für nicht einfache Eigenschaften Sätze Ruft die [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) -Methode des zugrunde liegenden Speichers auf und öffnet den "Content"-Stream erneut.</span><span class="sxs-lookup"><span data-stu-id="54ce3-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="54ce3-179">Bei einfachen Eigenschaften Sätzen wird nur E OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="54ce3-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="54ce3-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-181">Erstellt ein Enumeratorobjekt, das [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)implementiert. die Methoden von können aufgerufen werden, um die [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Wert-Strukturen aufzulisten, die Informationen zu den einzelnen Eigenschaften im Satz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="54ce3-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="54ce3-182">Diese Implementierung erstellt ein Array, in das der gesamte Eigenschaften Satz gelesen wird und der freigegeben werden kann, wenn [**ienumstatus propstg:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54ce3-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="54ce3-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-184">Füllt die Member einer Status- [**setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Struktur aus, die Informationen über die als Ganzes festgelegte Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="54ce3-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="54ce3-185">Stellt bei der Rückgabe einen Zeiger auf die-Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="54ce3-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="54ce3-186">Bei nicht einfachen Speicher Sätzen ruft diese Implementierung [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (oder [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) auf, um die Informationen aus dem zugrunde liegenden Speicher oder Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54ce3-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="54ce3-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="54ce3-188">Für nicht einfache Eigenschaften Sätze legt die vom zugrunde liegenden Speicher unterstützten Zeiten fest.</span><span class="sxs-lookup"><span data-stu-id="54ce3-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="54ce3-189">Diese Implementierung von [**settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) Ruft die [**IStorage:: setelementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) -Methode des zugrunde liegenden Speichers auf, um die Zeiten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="54ce3-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="54ce3-190">Es unterstützt die von der zugrunde liegenden Methode unterstützten Zeiten, die Änderungszeit, Zugriffszeit oder Erstellungszeit aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="54ce3-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="54ce3-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54ce3-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ce3-192">IPropertySetStorage-eigenständige Implementierung</span><span class="sxs-lookup"><span data-stu-id="54ce3-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="54ce3-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="54ce3-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="54ce3-194">**IStorage::/telementtimes**</span><span class="sxs-lookup"><span data-stu-id="54ce3-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="54ce3-195">**Stgopenpropstg**</span><span class="sxs-lookup"><span data-stu-id="54ce3-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="54ce3-196">**Stgkreatepropstg**</span><span class="sxs-lookup"><span data-stu-id="54ce3-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="54ce3-197">**Stgkreatepropsetstg**</span><span class="sxs-lookup"><span data-stu-id="54ce3-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 