---
description: Die imediaobjectimpl-Klassen Vorlage stellt eine Basis Implementierung für die imediaobject-Schnittstelle bereit. Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter Verwenden der DMO-Klassen Vorlage.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Imediaobjectimpl-Klassen Vorlage (dmuimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373871"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="453bb-104">Imediaobjectimpl-Klassen Vorlage</span><span class="sxs-lookup"><span data-stu-id="453bb-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="453bb-105">Die `IMediaObjectImpl` Klassen Vorlage stellt eine Basis Implementierung für die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="453bb-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="453bb-106">Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter [Verwenden der DMO-Klassen Vorlage](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="453bb-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="453bb-107">Diese `IMediaObjectImpl` Vorlage macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="453bb-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="453bb-108">-Klasse</span><span class="sxs-lookup"><span data-stu-id="453bb-108">Nested Class</span></span>                              | <span data-ttu-id="453bb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="453bb-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="453bb-110">**Sperren**</span><span class="sxs-lookup"><span data-stu-id="453bb-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="453bb-111">Hilfsklasse, die den DMO sperrt und entsperrt.</span><span class="sxs-lookup"><span data-stu-id="453bb-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="453bb-112">Methode</span><span class="sxs-lookup"><span data-stu-id="453bb-112">Method</span></span>                                                                      | <span data-ttu-id="453bb-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="453bb-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="453bb-114">[**Checktypesset**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="453bb-115">Bestimmt, ob alle nicht optionalen Streams über Medientypen verfügen.</span><span class="sxs-lookup"><span data-stu-id="453bb-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="453bb-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="453bb-117">Ruft den aktuellen Medientyp für einen angegebenen Eingabedaten Strom ab.</span><span class="sxs-lookup"><span data-stu-id="453bb-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="453bb-118">[**Inputtypeset**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="453bb-119">Fragt ab, ob der Medientyp für einen Eingabestream festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="453bb-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="453bb-120">[**Internalakzeptinginput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="453bb-121">Fragt ab, ob ein Eingabedaten Strom mehr Eingaben akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="453bb-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="453bb-122">[**Internalcheckinputtype**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="453bb-123">Fragt ab, ob ein Eingabedaten Strom einen bestimmten Medientyp annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="453bb-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="453bb-124">[**Internalcheckoutputtype**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="453bb-125">Fragt ab, ob ein Ausgabestream einen bestimmten Medientyp annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="453bb-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="453bb-126">[**Sperre**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="453bb-127">Sperrt den DMO.</span><span class="sxs-lookup"><span data-stu-id="453bb-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="453bb-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="453bb-129">Ruft den aktuellen Medientyp für einen angegebenen Ausgabestream ab.</span><span class="sxs-lookup"><span data-stu-id="453bb-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="453bb-130">[**Outputtypeset**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="453bb-131">Fragt ab, ob der Medientyp für einen Ausgabestream festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="453bb-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="453bb-132">[**Entsperren**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="453bb-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="453bb-133">Entsperrt den DMO</span><span class="sxs-lookup"><span data-stu-id="453bb-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="453bb-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="453bb-134">Requirements</span></span>



| <span data-ttu-id="453bb-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="453bb-135">Requirement</span></span> | <span data-ttu-id="453bb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="453bb-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="453bb-137">Header</span><span class="sxs-lookup"><span data-stu-id="453bb-137">Header</span></span><br/>  | <dl> <span data-ttu-id="453bb-138"><dt>Dmuimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="453bb-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="453bb-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="453bb-139">Library</span></span><br/> | <dl> <span data-ttu-id="453bb-140"><dt>Dmuguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="453bb-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="453bb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="453bb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453bb-142">DMO-Referenz</span><span class="sxs-lookup"><span data-stu-id="453bb-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="453bb-143">Verwenden der DMO-Klassen Vorlage</span><span class="sxs-lookup"><span data-stu-id="453bb-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
