---
description: Die getDescriptor-Methode gibt den von den Eingabe Parametern angegebenen USB-hubdeskriptor zurück.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: GetDescriptor-Methode der CIM_USBHub-Klasse (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958310"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="69266-103">GetDescriptor-Methode der CIM- \_ Klasse.</span><span class="sxs-lookup"><span data-stu-id="69266-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="69266-104">Die **getDescriptor** -Methode gibt den von den Eingabe Parametern angegebenen USB-hubdeskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="69266-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69266-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="69266-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="69266-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="69266-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="69266-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="69266-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="69266-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="69266-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="69266-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="69266-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="69266-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="69266-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69266-111">*RequestType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69266-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69266-112">Bit-zugeordneter Bezeichner für den Typ der deskriptoranforderung und den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="69266-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="69266-113">Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="69266-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="69266-114">*Requestvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69266-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69266-115">Enthält den Deskriptortyp im hohen Byte und den deskriptorindex (z. b. Index oder Offset im deskriptorarray) im unteren Byte.</span><span class="sxs-lookup"><span data-stu-id="69266-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="69266-116">Weitere Informationen finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="69266-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="69266-117">*RequestIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69266-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69266-118">Gibt den 2-Byte-sprach bezeichnercode an, der vom USB-Gerät beim Zurückgeben von Zeichen folgen deskriptordaten verwendet wird</span><span class="sxs-lookup"><span data-stu-id="69266-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="69266-119">Der-Parameter ist in der Regel 0 (null) für nicht Zeichen folgen Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="69266-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="69266-120">Weitere Informationen finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="69266-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="69266-121">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69266-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69266-122">Bei Eingabe die Länge (in Oktette) des Deskriptors, der zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="69266-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="69266-123">Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69266-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="69266-124">Wenn Sie größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69266-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="69266-125">Bei Ausgabe die Länge (in Oktette) des Puffers, der zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69266-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="69266-126">Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="69266-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="69266-127">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="69266-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69266-128">Der Puffer gibt die angeforderten Deskriptorinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="69266-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="69266-129">Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt des Puffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="69266-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69266-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69266-130">Return value</span></span>

<span data-ttu-id="69266-131">Gibt einen Wert von 0 (null) zurück, wenn der USB-Deskriptor erfolgreich zurückgegeben wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="69266-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="69266-132">In einer Unterklasse können die möglichen Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69266-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="69266-133">Die Zeichen folgen, auf die der Inhalt des " **fifqualifizierers** " übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69266-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="69266-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69266-134">Remarks</span></span>

<span data-ttu-id="69266-135">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="69266-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="69266-136">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="69266-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="69266-137">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69266-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="69266-138">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69266-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="69266-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69266-139">Requirements</span></span>



| <span data-ttu-id="69266-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69266-140">Requirement</span></span> | <span data-ttu-id="69266-141">Wert</span><span class="sxs-lookup"><span data-stu-id="69266-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69266-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69266-142">Minimum supported client</span></span><br/> | <span data-ttu-id="69266-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69266-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69266-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69266-144">Minimum supported server</span></span><br/> | <span data-ttu-id="69266-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69266-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69266-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="69266-146">Namespace</span></span><br/>                | <span data-ttu-id="69266-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="69266-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69266-148">Header</span><span class="sxs-lookup"><span data-stu-id="69266-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="69266-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69266-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="69266-150">MOF</span><span class="sxs-lookup"><span data-stu-id="69266-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69266-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69266-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69266-152">DLL</span><span class="sxs-lookup"><span data-stu-id="69266-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69266-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69266-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69266-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69266-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69266-155">**CIM-Startseite \_**</span><span class="sxs-lookup"><span data-stu-id="69266-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="69266-156">**CIM-Startseite \_**</span><span class="sxs-lookup"><span data-stu-id="69266-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

