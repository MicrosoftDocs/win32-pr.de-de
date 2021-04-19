---
description: Gibt den von den Eingabe Parametern angegebenen "tobdevice"-Deskriptor zurück.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: GetDescriptor-Methode der CIM_USBDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345887"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="58914-103">GetDescriptor-Methode der CIM_USBDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="58914-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="58914-104">Gibt den von den Eingabe Parametern angegebenen "tobdevice"-Deskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="58914-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="58914-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58914-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="58914-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58914-107">*RequestType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58914-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58914-108">Bitmap, die den Typ der deskriptoranforderung und den Empfänger angibt.</span><span class="sxs-lookup"><span data-stu-id="58914-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="58914-109">Der Typ der Anforderung kann "Standard", "Class" oder "Vendor-Specific" lauten.</span><span class="sxs-lookup"><span data-stu-id="58914-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="58914-110">Der Empfänger kann "Device", "Interface", "Endpoint" oder "Other" lauten.</span><span class="sxs-lookup"><span data-stu-id="58914-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="58914-111">Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="58914-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="58914-112">*Requestvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58914-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58914-113">Enthält den Deskriptortyp im hohen Byte und den deskriptorindex (z. b. Index oder Offset im deskriptorarray) im unteren Byte.</span><span class="sxs-lookup"><span data-stu-id="58914-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="58914-114">Weitere Informationen finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="58914-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="58914-115">*RequestIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58914-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58914-116">Definiert den 2-Byte-Sprach-ID-Code, der von "rbdevice" beim Zurückgeben von Zeichen folgen deskriptordaten</span><span class="sxs-lookup"><span data-stu-id="58914-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="58914-117">Der-Parameter ist in der Regel 0 für nicht-Zeichen folgen Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="58914-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="58914-118">Weitere Informationen finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="58914-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="58914-119">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="58914-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58914-120">Enthält bei Eingabe die Länge (in Oktette) des Deskriptors, der zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="58914-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="58914-121">Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58914-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="58914-122">Wenn Sie größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58914-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="58914-123">Bei der Ausgabe ist dieser Parameter die Länge des zurückgegebenen Puffers in Oktets.</span><span class="sxs-lookup"><span data-stu-id="58914-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="58914-124">Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="58914-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="58914-125">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58914-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58914-126">Gibt die angeforderten Deskriptorinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="58914-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="58914-127">Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt des Parameters nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="58914-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58914-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58914-128">Return value</span></span>

<span data-ttu-id="58914-129">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58914-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="58914-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58914-130">Requirements</span></span>



| <span data-ttu-id="58914-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58914-131">Requirement</span></span> | <span data-ttu-id="58914-132">Wert</span><span class="sxs-lookup"><span data-stu-id="58914-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58914-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58914-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58914-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="58914-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="58914-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58914-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58914-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="58914-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="58914-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="58914-137">Namespace</span></span><br/>                | <span data-ttu-id="58914-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="58914-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58914-139">MOF</span><span class="sxs-lookup"><span data-stu-id="58914-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58914-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58914-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58914-141">DLL</span><span class="sxs-lookup"><span data-stu-id="58914-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58914-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58914-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58914-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58914-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58914-144">**CIM-Start \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="58914-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




