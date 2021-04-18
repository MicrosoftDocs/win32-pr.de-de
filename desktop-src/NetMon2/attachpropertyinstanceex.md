---
description: Die attachpropertyinstanceex-Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschafts Daten.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Attachpropertyinstanceex-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358428"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="d9e46-103">Attachpropertyinstanceex-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9e46-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="d9e46-104">Die **attachpropertyinstanceex** -Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschafts Daten.</span><span class="sxs-lookup"><span data-stu-id="d9e46-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9e46-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d9e46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9e46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e46-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-108">Handle für den Frame, der analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9e46-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="d9e46-109">Verwenden Sie das Handle, das an die Parser-DLL im *hframe* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9e46-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-110">*hproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-111">Handle für eine [**PropertyInfo**](propertyinfo.md) -Struktur, die die Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="d9e46-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="d9e46-112">Beim Implementieren der [**Register**](register-parser.md) Export-Funktion geben Sie die **PropertyInfo** -Struktur an, die die Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="d9e46-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-113">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-114">Länge der Daten für diese Instanz der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d9e46-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-115">*lpdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-116">Ein Zeiger auf die Position in den erkannten Daten, in der sich der Eigenschafts Wert befindet.</span><span class="sxs-lookup"><span data-stu-id="d9e46-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="d9e46-117">Verwenden Sie den Zeiger, der an die Parser-DLL im *lpprotocol* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9e46-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-118">*Verlängert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-119">Länge der erweiterten Daten Länge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d9e46-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-120">*lpdataex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-121">Zeiger auf die erweiterten Daten, bei dem es sich in der Regel um eine Stapel Variable handelt, die die erweiterten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d9e46-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-122">*HelpID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-123">Bezeichner (von 0 bis 2047), der verwendet wird, um die kontextbezogene Hilfe für eine Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d9e46-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="d9e46-124">Die *HelpID* -Nummer ist relativ zur Hilfedatei, die der Protokoll [*Eigenschaften Datenbank*](p.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9e46-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-125">*Einzug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-126">Einzugs Ebene (von 0 bis 15) wird verwendet, um eine Eigenschaft hierarchisch anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d9e46-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="d9e46-127">Netzwerkmonitor verwendet die Ebenen 0 bis 9.</span><span class="sxs-lookup"><span data-stu-id="d9e46-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="d9e46-128">Ebene 15 ist ein spezieller Wert, der es dem Parser ermöglicht, eine verborgene Eigenschaft anzufügen, die nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="d9e46-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="d9e46-129">*IFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e46-130">Ein bitfeldwert, der die Reihenfolge der Bits innerhalb einer Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="d9e46-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="d9e46-131">Vorherige Parser, die *ferror* auf 0 oder 1 festgelegt haben, sollten nun *ferror* auf den iflag- \_ Fehler festlegen.</span><span class="sxs-lookup"><span data-stu-id="d9e46-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="d9e46-132">Legen Sie diesen Parameter auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="d9e46-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="d9e46-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d9e46-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d9e46-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d9e46-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="d9e46-135"><dt>**iflag- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="d9e46-136">Die Daten im Frame weisen einen Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d9e46-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="d9e46-137"><dt>**iflag wurde \_ ausgetauscht**</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="d9e46-138">Zum Anfüge Zeitpunkt ist **Word** Byte ein nicht-Intel-Format.</span><span class="sxs-lookup"><span data-stu-id="d9e46-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="d9e46-139"><dt>**iflag- \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="d9e46-140">Zum Anfüge Zeitpunkt ist die **Zeichenfolge** Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9e46-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e46-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9e46-141">Return value</span></span>

<span data-ttu-id="d9e46-142">Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="d9e46-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="d9e46-143">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="d9e46-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e46-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9e46-144">Remarks</span></span>

<span data-ttu-id="d9e46-145">Die " **attachpropertyinstanceex** "-Funktion wird während der Implementierung der " [**attachproperties**](attachproperties.md) "-Exportfunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d9e46-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="d9e46-146">Wenn eine Eigenschaft mithilfe von attachpropertyinstanceex an die Daten angefügt wird, erstellt Netzwerkmonitor eine [**propertyinst**](propertyinst.md) -Struktur, die die Instanz der angefügten Eigenschaft definiert, und eine [**propertyinstex**](propertyinstex.md) -Struktur, die die erweiterten Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="d9e46-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="d9e46-147">Wenn " **attachpropertyinstanceex** " aufgerufen wird und keine erweiterten Daten bereitgestellt werden, ist der *lpdataex* -Parameter **null** , oder der Parameter " *verlänex* " ist 0, der **attachpropertyinstanceex** -Aufruf ist funktional äquivalent zu einem [**attachpropertyinstance**](attachpropertyinstance.md) -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="d9e46-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="d9e46-148">Bei der Implementierung von [**attachproperties**](attachproperties.md)wird [**attachpropertyinstance**](attachpropertyinstance.md) aufgerufen, um die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d9e46-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="d9e46-149">Sie können auch die **attachpropertyinstanceex** -Funktion aufrufen, um die Eigenschaften Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d9e46-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="d9e46-150">Es wird jedoch empfohlen, dass Sie die Daten verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d9e46-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e46-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9e46-151">Requirements</span></span>



| <span data-ttu-id="d9e46-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9e46-152">Requirement</span></span> | <span data-ttu-id="d9e46-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d9e46-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e46-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9e46-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e46-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d9e46-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9e46-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e46-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9e46-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9e46-158">Header</span><span class="sxs-lookup"><span data-stu-id="d9e46-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9e46-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d9e46-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9e46-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9e46-161"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9e46-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d9e46-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9e46-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9e46-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




