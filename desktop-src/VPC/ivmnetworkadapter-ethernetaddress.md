---
title: Ivmnetworkadapter-ethernetaddress-Eigenschaft (vpccominterfaces. h)
description: Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Ethernetaddress-Eigenschaft virtueller PC
- Ethernetaddress-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, ethernetaddress-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739760"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="e5c6f-106">Ivmnetworkadapter:: ethernetaddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5c6f-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="e5c6f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e5c6f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e5c6f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e5c6f-109">Ruft die Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="e5c6f-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c6f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5c6f-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="e5c6f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e5c6f-112">Property value</span></span>

<span data-ttu-id="e5c6f-113">Die Mac-Adresse der virtuellen NIC.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="e5c6f-114">Er sollte das Format "*xx* XX XX XX XX -  -  -  -  - *xx*" aufweisen, wobei jedes *X* eine hexadezimale Ziffer ist.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5c6f-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e5c6f-115">Error codes</span></span>



| <span data-ttu-id="e5c6f-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e5c6f-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="e5c6f-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e5c6f-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5c6f-118"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="e5c6f-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e5c6f-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="e5c6f-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e5c6f-122"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="e5c6f-123">Der-Parameter weist nicht das richtige Format auf.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="e5c6f-124"><dt>VM \_ E \_ cant \_ \_ dynamische \_ Mac- \_ Adresse</dt> <dt>0xa004070a</dt> festlegen</span><span class="sxs-lookup"><span data-stu-id="e5c6f-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="e5c6f-125">Die Ethernet-Adresse für eine Netzwerkschnittstelle kann entweder dynamisch generiert werden, oder Sie kann vom Benutzer auf eine statische Adresse festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="e5c6f-126">Diese Methode kann nicht aufgerufen werden, wenn die Adresse für die dynamische Generierung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="e5c6f-127">Die [**isethernetaddressdynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) -Eigenschaft wird verwendet, um das Generierungs Verhalten der Ethernet-Adresse zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="e5c6f-128"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="e5c6f-129">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-129">The virtual machine was not found.</span></span> <span data-ttu-id="e5c6f-130">Dies kann vorkommen, wenn der Computer entfernt wurde, nachdem das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="e5c6f-131"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="e5c6f-132">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="e5c6f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5c6f-133">Requirements</span></span>



| <span data-ttu-id="e5c6f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5c6f-134">Requirement</span></span> | <span data-ttu-id="e5c6f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e5c6f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c6f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5c6f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c6f-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5c6f-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5c6f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5c6f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c6f-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5c6f-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e5c6f-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e5c6f-140">End of client support</span></span><br/>    | <span data-ttu-id="e5c6f-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5c6f-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e5c6f-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="e5c6f-142">Product</span></span><br/>                  | <span data-ttu-id="e5c6f-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e5c6f-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e5c6f-144">Header</span><span class="sxs-lookup"><span data-stu-id="e5c6f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c6f-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c6f-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e5c6f-146">IID</span><span class="sxs-lookup"><span data-stu-id="e5c6f-146">IID</span></span><br/>                      | <span data-ttu-id="e5c6f-147">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="e5c6f-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e5c6f-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5c6f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c6f-149">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="e5c6f-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

