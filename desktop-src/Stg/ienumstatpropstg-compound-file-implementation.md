---
title: Implementierung der IEnumSTATPROPSTG-Compound Datei
description: Die Implementierung der Verbund Datei der ienumstatus propstg-Schnittstelle wird zum Auflisten von Eigenschaften verwendet. Dies führt zu Status Werten, die statistische Eigenschaften Daten enthalten.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- Ienumstatus propstg-Schnittstellen-Erweiterung, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949015"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="9b8fa-104">Implementierung der IEnumSTATPROPSTG-Compound Datei</span><span class="sxs-lookup"><span data-stu-id="9b8fa-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="9b8fa-105">Die Implementierung der Verbund Datei der [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Schnittstelle wird zum Auflisten von Eigenschaften verwendet. Dies führt zu [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Werten, die statistische Eigenschaften Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="9b8fa-106">Die Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) verwaltet die statistischen Daten und ist einem aktuellen Verbund Datei-Speicher Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="9b8fa-107">Der Konstruktor in der com-Implementierung von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) erstellt eine Klasse, die den gesamten Eigenschaften Satz liest und ein statisches Array erstellt, das freigegeben werden kann, wenn **ienumstatus propstg:: Clone** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="9b8fa-108">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="9b8fa-108">When to Use</span></span>

<span data-ttu-id="9b8fa-109">Aufrufen der Implementierung der Verbund Datei von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) zum Auflisten der [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Wert Strukturen, die Daten zu den Eigenschaften innerhalb des aktuellen Eigenschaften Satzes enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="9b8fa-110">Wenn Sie die Verbund Datei Implementierung der Eigenschaften Speicher Schnittstellen verwenden, müssen Sie [**IPropertyStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) aufrufen, um einen Zeiger auf **ienumstatus propstg** zurückzugeben, um das Eigenschaften Speicher Objekt und die darin enthaltenen Elemente zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b8fa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b8fa-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="9b8fa-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**Ienumstatus propstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="9b8fa-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="9b8fa-113">Ruft das nächste oder mehrere [**Status-g**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Strukturen ab (die Zahl wird durch den *celt* -Parameter angegeben).</span><span class="sxs-lookup"><span data-stu-id="9b8fa-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="9b8fa-114">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="9b8fa-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**Ienumstatus propstg:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="9b8fa-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="9b8fa-116">Überspringt die Anzahl der in *celt* angegebenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="9b8fa-117">Das nächste Element, das durch einen-aufzurufenden aufgerufen werden soll, wird das-Element nach den übersprungenen Elementen.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="9b8fa-118">Gibt s \_ OK zurück, wenn *celt* -Elemente übersprungen wurden; gibt den Wert false zurück, \_ Wenn weniger als *celt* -Elemente übersprungen wurden.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="9b8fa-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**Ienumstatus propstg:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="9b8fa-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="9b8fa-120">Legt den Cursor auf den Anfang der Enumeration fest.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="9b8fa-121">Wenn erfolgreich, wird S OK zurückgegeben; \_ andernfalls wird STG \_ E \_ InvalidHandle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="9b8fa-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**Ienumstatus propstg:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="9b8fa-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="9b8fa-123">Verwendet den Konstruktor für [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , um eine Kopie des Arrays zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="9b8fa-124">Da die-Klasse, die das statische Array erstellt, tatsächlich das-Objekt enthält, fügt diese Funktion hauptsächlich den Verweis Zähler hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b8fa-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9b8fa-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b8fa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b8fa-126">**Status-g**</span><span class="sxs-lookup"><span data-stu-id="9b8fa-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="9b8fa-127">**IPropertyStorage:: Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="9b8fa-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 