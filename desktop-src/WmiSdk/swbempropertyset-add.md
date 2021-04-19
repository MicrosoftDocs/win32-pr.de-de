---
description: Die Add-Methode des-Objekts von "Swap PropertySet" fügt der Auflistung von "gobempropertyset" ein "taubemproperty"-Objekt hinzu. Wenn eine Eigenschaft mit demselben Namen bereits in der Auflistung vorhanden ist, wird der Inhalt durch die neue Definition ersetzt.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Methode "gobempropertyset. Add" (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369041"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="2dd1b-104">Taubempropertyset. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="2dd1b-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="2dd1b-105">Die **Add** -Methode des-Objekts von " [**Swap PropertySet**](swbempropertyset.md) " fügt der Auflistung von " **gobempropertyset** " ein " [**taubemproperty**](swbemproperty.md) "-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="2dd1b-106">Wenn eine Eigenschaft mit demselben Namen bereits in der Auflistung vorhanden ist, wird der Inhalt durch die neue Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="2dd1b-107">Der Wert der hinzugefügten Eigenschaft ist nach diesem Vorgang **null** (nicht zugewiesen).</span><span class="sxs-lookup"><span data-stu-id="2dd1b-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="2dd1b-108">Um den Wert einer WMI-Eigenschaft festzulegen oder zu ändern, müssen Sie die [**value**](swbemdatetime-value.md) -Eigenschaft des zurückgegebenen " [**taubemproperty**](swbemproperty.md) "-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="2dd1b-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2dd1b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd1b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd1b-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2dd1b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd1b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd1b-112">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="2dd1b-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-113">Required.</span></span> <span data-ttu-id="2dd1b-114">Der Name der neuen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-115">*icimtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd1b-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-116">Required.</span></span> <span data-ttu-id="2dd1b-117">Eine ganze Zahl, die den **CimType-Qualifizierer** der neuen Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="2dd1b-118">Die Liste mit den **CimType-Qualifizierern** und deren Werten finden Sie unter [**wbemcimtypeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) .</span><span class="sxs-lookup"><span data-stu-id="2dd1b-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-119">*bisarray* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2dd1b-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-120">Gibt an, ob die Eigenschaft ein Arraytyp ist.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="2dd1b-121">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-122">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2dd1b-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-123">Reserviert und muss NULL sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd1b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2dd1b-124">Return value</span></span>

<span data-ttu-id="2dd1b-125">Bei erfolgreicher Ausführung gibt diese Methode ein-Objekt zurück, das die neue [**-Eigenschaft darstellt**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd1b-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="2dd1b-126">Andernfalls wird ein **null** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2dd1b-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2dd1b-127">Error codes</span></span>

<span data-ttu-id="2dd1b-128">Nach Abschluss der **Add** -Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2dd1b-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-130">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-131">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-132">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-133">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-134">Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="2dd1b-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="2dd1b-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="2dd1b-136">Der **CimType-Qualifizierer** wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2dd1b-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dd1b-137">Examples</span></span>

<span data-ttu-id="2dd1b-138">Ein Codebeispiel, in dem diese Methode verwendet wird, finden Sie im Thema zu " [**Swap-PropertySet**](swbempropertyset.md) ".</span><span class="sxs-lookup"><span data-stu-id="2dd1b-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd1b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dd1b-139">Requirements</span></span>



| <span data-ttu-id="2dd1b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dd1b-140">Requirement</span></span> | <span data-ttu-id="2dd1b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2dd1b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd1b-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd1b-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2dd1b-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2dd1b-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd1b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dd1b-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2dd1b-146">Header</span><span class="sxs-lookup"><span data-stu-id="2dd1b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dd1b-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd1b-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dd1b-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2dd1b-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2dd1b-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2dd1b-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2dd1b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd1b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dd1b-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd1b-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2dd1b-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="2dd1b-152">CLSID</span></span><br/>                    | <span data-ttu-id="2dd1b-153">CLSID- \_ Swap-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="2dd1b-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="2dd1b-154">IID</span><span class="sxs-lookup"><span data-stu-id="2dd1b-154">IID</span></span><br/>                      | <span data-ttu-id="2dd1b-155">IID \_ iswbempropertyset</span><span class="sxs-lookup"><span data-stu-id="2dd1b-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="2dd1b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dd1b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd1b-157">**Swap PropertySet**</span><span class="sxs-lookup"><span data-stu-id="2dd1b-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="2dd1b-158">**' Swap PropertySet. Remove '**</span><span class="sxs-lookup"><span data-stu-id="2dd1b-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="2dd1b-159">**Swap Property. Value**</span><span class="sxs-lookup"><span data-stu-id="2dd1b-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




