---
description: Die neue Methode initialisiert einen Befehl, der ausgeführt werden soll, und gibt ein neues cdeferredcommand-Objekt zurück.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Ccmdqueue. New-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361287"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="97579-103">Ccmdqueue. New-Methode</span><span class="sxs-lookup"><span data-stu-id="97579-103">CCmdQueue.New method</span></span>

<span data-ttu-id="97579-104">Die `New` -Methode initialisiert einen Befehl, der ausgeführt werden soll, und gibt ein neues [**cdeferredcommand**](cdeferredcommand.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="97579-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97579-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97579-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="97579-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97579-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="97579-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-108">Adresse eines Zeigers auf ein [**cdeferredcommand**](cdeferredcommand.md) -Objekt, mit dem eine Anwendung den Befehl abbrechen kann, eine neue Präsentationszeit für Sie festgelegt oder Schätz Informationen abruft.</span><span class="sxs-lookup"><span data-stu-id="97579-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="97579-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="97579-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-110">Zeiger auf das Objekt, von dem der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97579-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="97579-111">*time*</span><span class="sxs-lookup"><span data-stu-id="97579-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-112">Der Zeitpunkt, zu dem der Befehl oder die Befehle in der Warteschlange ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97579-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="97579-113">*IID*</span><span class="sxs-lookup"><span data-stu-id="97579-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-114">Zeiger auf den Globally Unique Identifier (**GUID**) der aufzurufenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="97579-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="97579-115">*dispidmethod*</span><span class="sxs-lookup"><span data-stu-id="97579-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-116">Methode für die aufzurufende Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="97579-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="97579-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="97579-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-118">Flags, die den Kontext des Aufrufs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="97579-118">Flags describing the context of the call.</span></span> <span data-ttu-id="97579-119">Dieser Parameter unterstützt dieselben Flags wie die **IDispatch:: Aufrufen** -Methode.</span><span class="sxs-lookup"><span data-stu-id="97579-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="97579-120">*kargs*</span><span class="sxs-lookup"><span data-stu-id="97579-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-121">Anzahl der über gebenen Argumente.</span><span class="sxs-lookup"><span data-stu-id="97579-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="97579-122">*pdispparameams*</span><span class="sxs-lookup"><span data-stu-id="97579-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-123">Ein Zeiger auf die Liste der Variant-Typen, die den Dispatch-Parametern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="97579-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="97579-124">*pVarResult*</span><span class="sxs-lookup"><span data-stu-id="97579-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-125">Ein Zeiger auf die Liste, in der Ergebnisse (sofern vorhanden) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97579-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="97579-126">*gibt puArgErr*</span><span class="sxs-lookup"><span data-stu-id="97579-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-127">Zeiger auf den Index in der *pdispparameams* -Parameterliste, in der der letzte Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="97579-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="97579-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="97579-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="97579-129">Ein Wert, der angibt, ob der *Zeit* Parameter ein streamzeitwert (**true**) oder ein Präsentations Zeitwert (**false**) ist.</span><span class="sxs-lookup"><span data-stu-id="97579-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97579-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97579-130">Return value</span></span>

<span data-ttu-id="97579-131">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="97579-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="97579-132">Gibt "E outo-Memory" zurück, \_ Wenn *ppcmd* von der Erstellung des neuen [**cdeferredcommand**](cdeferredcommand.md) -Objekts mit dem Wert " **null**" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97579-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="97579-133">Andernfalls gibt ein **HRESULT** zurück, das einen Fehler beim Versuch angibt, ein neues **cdeferredcommand** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97579-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="97579-134">Wenn ein Fehler vorliegt, wurde kein Objekt in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="97579-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="97579-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97579-135">Remarks</span></span>

<span data-ttu-id="97579-136">Das neue [**cdeferredcommand**](cdeferredcommand.md) -Objekt wird mit den Parametern initialisiert und während der Erstellung der Warteschlange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97579-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="97579-137">Diese Methode ähnelt der **IDispatch:: Aufrufen** -Methode.</span><span class="sxs-lookup"><span data-stu-id="97579-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="97579-138">Die Werte für den *wFlags* -Parameter umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97579-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="97579-139">Wert</span><span class="sxs-lookup"><span data-stu-id="97579-139">Value</span></span>                    | <span data-ttu-id="97579-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97579-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97579-141">Dispatch- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="97579-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="97579-142">Der Member wird als Methode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97579-142">The member is being run as a method.</span></span> <span data-ttu-id="97579-143">Wenn eine Eigenschaft denselben Namen hat, können sowohl dieses als auch das Dispatch \_ PropertyGet-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="97579-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="97579-144">Dispatch- \_ PropertyGet</span><span class="sxs-lookup"><span data-stu-id="97579-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="97579-145">Der Member wird als Eigenschaft oder Datenmember abgerufen.</span><span class="sxs-lookup"><span data-stu-id="97579-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="97579-146">Dispatch- \_ PropertyPut</span><span class="sxs-lookup"><span data-stu-id="97579-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="97579-147">Der Member wird als Eigenschaft oder Datenmember geändert.</span><span class="sxs-lookup"><span data-stu-id="97579-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="97579-148">Dispatch \_ propertyputref</span><span class="sxs-lookup"><span data-stu-id="97579-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="97579-149">Der Member wird über eine Verweis Zuweisung und nicht über eine Wert Zuweisung geändert.</span><span class="sxs-lookup"><span data-stu-id="97579-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="97579-150">Dieser Wert ist nur gültig, wenn die-Eigenschaft einen Verweis auf ein-Objekt akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="97579-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="97579-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97579-151">Requirements</span></span>



| <span data-ttu-id="97579-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97579-152">Requirement</span></span> | <span data-ttu-id="97579-153">Wert</span><span class="sxs-lookup"><span data-stu-id="97579-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97579-154">Header</span><span class="sxs-lookup"><span data-stu-id="97579-154">Header</span></span><br/>  | <dl> <span data-ttu-id="97579-155"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97579-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="97579-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97579-156">Library</span></span><br/> | <dl> <span data-ttu-id="97579-157">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="97579-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97579-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97579-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97579-159">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="97579-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




