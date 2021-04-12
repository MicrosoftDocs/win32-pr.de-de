---
description: Beschreibt, wie die allgemeinen Methoden der Auflistungs Schnittstellen verwendet werden.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Arbeiten mit XPS OM-Sammlungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216630"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="22894-103">Arbeiten mit XPS OM-Sammlungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="22894-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="22894-104">Beschreibt, wie die allgemeinen Methoden der Auflistungs Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22894-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="22894-105">Inhalte</span><span class="sxs-lookup"><span data-stu-id="22894-105">Contents</span></span>

<span data-ttu-id="22894-106">Die in diesem Abschnitt beschriebenen Methoden werden in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22894-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="22894-107">Nicht alle Sammlungs Schnittstellen unterstützen diese Methoden, und einige Schnittstellen unterstützen auch Methoden, die nicht auf dieser Seite beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="22894-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="22894-108">Eine Liste der Methoden, die von einer bestimmten Schnittstelle unterstützt werden, finden Sie in der Beschreibung der Beschreibung der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22894-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="22894-109">Append-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="22894-110">GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="22894-111">GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="22894-112">InsertAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="22894-113">RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="22894-114">Methode "-Methode"</span><span class="sxs-lookup"><span data-stu-id="22894-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="22894-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22894-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="22894-116">Append-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-116">Append Method</span></span>

<span data-ttu-id="22894-117">Fügt ein Objekt an das Ende der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="22894-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="22894-118">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="22894-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-119">**Description**</span></span>

<span data-ttu-id="22894-120">Am Ende der Auflistung fügt diese Methode ein Objekt an, das in der Parameterliste übergeben wird, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="22894-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![eine Abbildung, die zeigt, wie Anfügen der Auflistung einen Eintrag hinzufügt.](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="22894-122">GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-122">GetAt Method</span></span>

<span data-ttu-id="22894-123">Ruft ein-Objekt von einer angegebenen Position in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="22894-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="22894-124">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="22894-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-125">**Description**</span></span>

<span data-ttu-id="22894-126">Schreibt das-Objekt, das am durch *Index* angegebenen Speicherort der Auflistung gespeichert ist, in die Variable, auf die vom- *Objekt* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="22894-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="22894-127">Durch diese Aktion wird der Inhalt der Sammlung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="22894-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="22894-128">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22894-128">The following diagram illustrates this process.</span></span>

![eine Abbildung, die zeigt, wie GetAt einen Eintrag aus der Auflistung abruft.](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="22894-130">GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-130">GetCount Method</span></span>

<span data-ttu-id="22894-131">Ruft die Anzahl der-Objekte ab, die in der Auflistung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="22894-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="22894-132">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="22894-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-133">**Description**</span></span>

<span data-ttu-id="22894-134">Schreibt die Anzahl der-Objekte, die zurzeit in der Auflistung gespeichert sind, in die Variable, auf die von *count* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="22894-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="22894-135">Durch diese Aktion wird der Inhalt der Sammlung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="22894-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="22894-136">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22894-136">The following diagram illustrates this process.</span></span>

![eine Abbildung, die zeigt, wie GetCount die Anzahl der Einträge in der Auflistung abruft.](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="22894-138">InsertAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-138">InsertAt Method</span></span>

<span data-ttu-id="22894-139">Fügt ein-Objekt an einer angegebenen Position der Auflistung ein.</span><span class="sxs-lookup"><span data-stu-id="22894-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="22894-140">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="22894-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-141">**Description**</span></span>

<span data-ttu-id="22894-142">Das Objekt, das in das- *Objekt* übermittelt wird, wird in die-Auflistung an der durch den *Index* angegebenen Position eingefügt.</span><span class="sxs-lookup"><span data-stu-id="22894-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="22894-143">Bevor das neue- *Objekt* eingefügt wird, verschiebt diese Methode um 1 das Objekt, das die Position zuvor am *Index* belegt hat, und verschiebt alle Schnittstellen Zeiger nach dem *Index*.</span><span class="sxs-lookup"><span data-stu-id="22894-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="22894-144">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22894-144">The following diagram illustrates this process.</span></span>

![eine Abbildung, die zeigt, wie InsertAt der Auflistung einen Eintrag hinzufügt.](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="22894-146">RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="22894-146">RemoveAt Method</span></span>

<span data-ttu-id="22894-147">Entfernt das-Objekt aus einer angegebenen Position in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="22894-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="22894-148">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="22894-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-149">**Description**</span></span>

<span data-ttu-id="22894-150">Diese Methode gibt das Objekt aus der durch den *Index* angegebenen Position frei und komprimiert dann die Auflistung, indem Sie um 1 den Index jedes Zeigers nach dem *Index* reduziert.</span><span class="sxs-lookup"><span data-stu-id="22894-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="22894-151">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22894-151">The following diagram illustrates this process.</span></span>

![eine Abbildung, die zeigt, wie RemoveAt einen Eintrag aus der Sammlung entfernt](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="22894-153">Methode "-Methode"</span><span class="sxs-lookup"><span data-stu-id="22894-153">SetAt Method</span></span>

<span data-ttu-id="22894-154">Ersetzt das-Objekt an einer angegebenen Position in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="22894-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="22894-155">**Generische Syntax**</span><span class="sxs-lookup"><span data-stu-id="22894-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="22894-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22894-156">**Description**</span></span>

<span data-ttu-id="22894-157">Diese Methode gibt zuerst das Objekt an dem Speicherort aus, auf den der *Index* verweist, und ersetzt dieses Objekt dann durch das Objekt, das im- *Objekt* weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="22894-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="22894-158">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22894-158">The following diagram illustrates this process.</span></span>

![eine Abbildung, die zeigt, wie das-enumerationszeichen einen Eintrag in der Auflistung ersetzt](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="22894-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22894-160">See Also</span></span>

<dl>

[<span data-ttu-id="22894-161">**Ixpsomcolorprofileresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="22894-162">**Ixpsomdashcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="22894-163">**Ixpsomdocumentcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="22894-164">**Ixpsomfontresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="22894-165">**Ixpsomgeometryfigurückruf**</span><span class="sxs-lookup"><span data-stu-id="22894-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="22894-166">**Ixpsomgradientstopcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="22894-167">**Ixpsomimageresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="22894-168">**Ixpsomnamecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="22894-169">**Ixpsompagereferencecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="22894-170">**Ixpsomparamecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="22894-171">**Ixpsomremotediktattionaryresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="22894-172">**Ixpsomsignatureblockresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="22894-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="22894-173">**Ixpsomvisualcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="22894-174">**Ixpssignatureblockcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="22894-175">**Ixpssignaturückruf**</span><span class="sxs-lookup"><span data-stu-id="22894-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="22894-176">**Ixpssignaturerequestcollection**</span><span class="sxs-lookup"><span data-stu-id="22894-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



