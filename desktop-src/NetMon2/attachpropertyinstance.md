---
description: Die attachpropertyinstance-Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Attachpropertyinstance-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867031"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="d48c4-103">Attachpropertyinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d48c4-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="d48c4-104">Die **attachpropertyinstance** -Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu.</span><span class="sxs-lookup"><span data-stu-id="d48c4-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48c4-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d48c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d48c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48c4-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-108">Handle für den Frame, der analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="d48c4-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="d48c4-109">Verwenden Sie das Handle, das an die Parser-DLL im *hframe* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d48c4-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-110">*hproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-111">Handle für eine [**PropertyInfo**](propertyinfo.md) -Struktur, die die Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="d48c4-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="d48c4-112">Beim Implementieren der [**Register**](register-parser.md) Export-Funktion geben Sie die **PropertyInfo** -Struktur an, die die Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="d48c4-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-113">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-114">Länge der Daten für diese Instanz der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d48c4-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-115">*lpdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-116">Ein Zeiger auf die Position in den erkannten Daten, in der sich der Eigenschafts Wert befindet.</span><span class="sxs-lookup"><span data-stu-id="d48c4-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="d48c4-117">Verwenden Sie den Zeiger, der an die Parser-DLL im *lpprotocol* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d48c4-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-118">*HelpID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-119">Bezeichner (von 0 bis 2047), der verwendet wird, um die kontextbezogene Hilfe für die Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d48c4-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="d48c4-120">Die Bezeichnernummer ist relativ zur Hilfedatei, die der Protokoll [*Eigenschaften Datenbank*](p.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d48c4-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-121">*Einzug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-122">Einzugs Ebene (von 0 bis 15) wird verwendet, um eine Eigenschaft hierarchisch anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d48c4-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="d48c4-123">Netzwerkmonitor verwendet die Ebenen 0 bis 14, um Eigenschaften einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d48c4-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="d48c4-124">Ebene 15 ist ein spezieller Wert, der es einem Parser ermöglicht, eine verborgene Eigenschaft anzufügen, die nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="d48c4-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="d48c4-125">*IFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c4-126">Ein bitfeldwert, der die Reihenfolge der Bits innerhalb einer Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="d48c4-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="d48c4-127">Vorherige Parser, die *ferror* auf 0 oder 1 festgelegt haben, sollten nun *ferror* auf den iflag- \_ Fehler festlegen.</span><span class="sxs-lookup"><span data-stu-id="d48c4-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="d48c4-128">Legen Sie diesen Parameter auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="d48c4-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="d48c4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d48c4-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d48c4-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d48c4-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="d48c4-131"><dt>**iflag- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="d48c4-132">Die Daten im Frame weisen einen Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d48c4-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="d48c4-133"><dt>**iflag wurde \_ ausgetauscht**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="d48c4-134">Zum Anfüge Zeitpunkt ist **Word** Byte ein nicht-Intel-Format.</span><span class="sxs-lookup"><span data-stu-id="d48c4-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="d48c4-135"><dt>**iflag- \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="d48c4-136">Zum Anfüge Zeitpunkt ist die **Zeichenfolge** Unicode.</span><span class="sxs-lookup"><span data-stu-id="d48c4-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48c4-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d48c4-137">Return value</span></span>

<span data-ttu-id="d48c4-138">Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="d48c4-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="d48c4-139">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="d48c4-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d48c4-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d48c4-140">Remarks</span></span>

<span data-ttu-id="d48c4-141">Die **attachpropertyinstance** -Funktion wird während der Implementierung der [**attachproperties**](attachproperties.md) -Exportfunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d48c4-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="d48c4-142">Wenn eine Eigenschaft an die Daten angefügt wird, erstellt Netzwerkmonitor eine [**propertyinst**](propertyinst.md) -Struktur, die die Instanz der angefügten Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="d48c4-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="d48c4-143">Bei der Implementierung von [**attachproperties**](attachproperties.md)wird **attachpropertyinstance** aufgerufen, um die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d48c4-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="d48c4-144">Sie können auch die [**attachpropertyinstanceex**](attachpropertyinstanceex.md) -Funktion aufrufen, um die Eigenschaften Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d48c4-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="d48c4-145">Es wird jedoch empfohlen, dass Sie die Daten verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d48c4-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="d48c4-146">Informationen zu</span><span class="sxs-lookup"><span data-stu-id="d48c4-146">For Information on</span></span>                                        | <span data-ttu-id="d48c4-147">Siehe</span><span class="sxs-lookup"><span data-stu-id="d48c4-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d48c4-148">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d48c4-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="d48c4-149">**Parser**</span><span class="sxs-lookup"><span data-stu-id="d48c4-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="d48c4-150">Aufrufen von " **attachpropertyinstance**".</span><span class="sxs-lookup"><span data-stu-id="d48c4-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="d48c4-151">Implementieren von attachproperties</span><span class="sxs-lookup"><span data-stu-id="d48c4-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="d48c4-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48c4-152">Requirements</span></span>



| <span data-ttu-id="d48c4-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48c4-153">Requirement</span></span> | <span data-ttu-id="d48c4-154">Wert</span><span class="sxs-lookup"><span data-stu-id="d48c4-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d48c4-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d48c4-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d48c4-156">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d48c4-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d48c4-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d48c4-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d48c4-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d48c4-159">Header</span><span class="sxs-lookup"><span data-stu-id="d48c4-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d48c4-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d48c4-161">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d48c4-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="d48c4-162"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d48c4-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d48c4-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48c4-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48c4-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48c4-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d48c4-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48c4-166">**Attachproperties**</span><span class="sxs-lookup"><span data-stu-id="d48c4-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="d48c4-167">**Attachpropertyinstanceex**</span><span class="sxs-lookup"><span data-stu-id="d48c4-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="d48c4-168">**Propertyinst**</span><span class="sxs-lookup"><span data-stu-id="d48c4-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




