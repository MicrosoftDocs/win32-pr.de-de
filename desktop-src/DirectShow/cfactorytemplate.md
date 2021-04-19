---
description: Bietet eine Vorlage zum Erstellen von Klassenfactorys.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Cfactorytemplate-Klasse (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359639"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="21f8f-103">Cfactorytemplate-Klasse</span><span class="sxs-lookup"><span data-stu-id="21f8f-103">CFactoryTemplate class</span></span>

<span data-ttu-id="21f8f-104">Bietet eine Vorlage zum Erstellen von Klassenfactorys.</span><span class="sxs-lookup"><span data-stu-id="21f8f-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="21f8f-105">In DirectShow werden **Klassenfactorys mithilfe der cfactorytemplate** -Klasse, die auch als Factoryvorlage bezeichnet wird, spezialisiert. </span><span class="sxs-lookup"><span data-stu-id="21f8f-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="21f8f-106">Jede Klassenfactory enthält einen Zeiger auf eine Factoryvorlage.</span><span class="sxs-lookup"><span data-stu-id="21f8f-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="21f8f-107">Die Factoryvorlage enthält Informationen über ein COM-Objekt, einschließlich des Klassen Bezeichners (CLSID) des Objekts und eines Zeigers auf eine Funktion, die das Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="21f8f-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="21f8f-108">Deklarieren Sie in der dll ein globales Array von fabricvorlagen mit dem Namen *g- \_ Vorlagen*.</span><span class="sxs-lookup"><span data-stu-id="21f8f-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="21f8f-109">Fügen Sie für jedes Objekt in der DLL eine Factory-Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="21f8f-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="21f8f-110">Wenn die [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion eine neue Klassenfactory erstellt, durchsucht Sie das Array nach einer Vorlage mit einer entsprechenden CLSID.</span><span class="sxs-lookup"><span data-stu-id="21f8f-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="21f8f-111">Wenn Sie einen gefunden hat, wird eine Klassenfactory erstellt, die einen Zeiger auf die entsprechende Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="21f8f-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="21f8f-112">Wenn der Client **IClassFactory:: kreateinstance** aufruft, ruft die Klassenfactory die in der Vorlage definierte instanzizierungsfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="21f8f-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="21f8f-113">Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="21f8f-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="21f8f-114">Öffentliche Element Variablen</span><span class="sxs-lookup"><span data-stu-id="21f8f-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="21f8f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21f8f-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="21f8f-116">**m- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="21f8f-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="21f8f-117">Name des Filters.</span><span class="sxs-lookup"><span data-stu-id="21f8f-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="21f8f-118">**m \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="21f8f-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="21f8f-119">Zeiger auf die CLSID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21f8f-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="21f8f-120">**m \_ lpfnnew**</span><span class="sxs-lookup"><span data-stu-id="21f8f-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="21f8f-121">Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="21f8f-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="21f8f-122">**m \_ lpfninit**</span><span class="sxs-lookup"><span data-stu-id="21f8f-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="21f8f-123">Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21f8f-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="21f8f-124">**m- \_ pamoviesetup- \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="21f8f-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="21f8f-125">Zeiger auf eine [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="21f8f-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="21f8f-126">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="21f8f-126">Public Methods</span></span>                                                            | <span data-ttu-id="21f8f-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21f8f-127">Description</span></span>                                                                |
| [<span data-ttu-id="21f8f-128">**Isclassid**</span><span class="sxs-lookup"><span data-stu-id="21f8f-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="21f8f-129">Bestimmt, ob eine CLSID dieser Klassen Vorlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="21f8f-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="21f8f-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="21f8f-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="21f8f-131">Ruft die Objekt Erstellungs Funktion für die-Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="21f8f-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="21f8f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21f8f-132">Requirements</span></span>



| <span data-ttu-id="21f8f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21f8f-133">Requirement</span></span> | <span data-ttu-id="21f8f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="21f8f-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f8f-135">Header</span><span class="sxs-lookup"><span data-stu-id="21f8f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="21f8f-136"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21f8f-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="21f8f-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21f8f-137">Library</span></span><br/> | <dl> <span data-ttu-id="21f8f-138">" <dt>Ermbase. lib;</dt> " " <dt>Straumbasd. lib</dt> "</span><span class="sxs-lookup"><span data-stu-id="21f8f-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f8f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21f8f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f8f-140">Basisklassen Referenz</span><span class="sxs-lookup"><span data-stu-id="21f8f-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

