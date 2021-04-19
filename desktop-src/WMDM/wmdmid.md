---
title: Wmdmid-Struktur
description: Die wmdmid-Struktur beschreibt Seriennummern und Gruppen-IDs.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Wmdmid-Struktur Windows Media Device Manager
- Pwmdmid-Struktur Zeiger Windows Media-Device Manager
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359792"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="70a39-105">Wmdmid-Struktur</span><span class="sxs-lookup"><span data-stu-id="70a39-105">WMDMID structure</span></span>

<span data-ttu-id="70a39-106">Die **wmdmid** -Struktur beschreibt Seriennummern und Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="70a39-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="70a39-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="70a39-108">Member</span><span class="sxs-lookup"><span data-stu-id="70a39-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70a39-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="70a39-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="70a39-110">Größe der **wmdmid** -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="70a39-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="70a39-111">**dwvendorid**</span><span class="sxs-lookup"><span data-stu-id="70a39-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="70a39-112">**DWORD** , das die registrierte ID-Nummer des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="70a39-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="70a39-113">Enthält 0 (null), wenn Sie nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70a39-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="70a39-114">**Länge der PID- \[ wmdmid \_\]**</span><span class="sxs-lookup"><span data-stu-id="70a39-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="70a39-115">Ein Zeiger auf ein Bytearray, das die Seriennummer enthält.</span><span class="sxs-lookup"><span data-stu-id="70a39-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="70a39-116">Die Seriennummer ist eine Zeichenfolge von Byte Werten, die kein Standardformat aufweisen.</span><span class="sxs-lookup"><span data-stu-id="70a39-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="70a39-117">Beachten Sie, dass es sich hierbei nicht um einen breit Zeichen Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="70a39-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="70a39-118">**Wmdmid \_ LENGTH** ist ein konstanter Wert, der in "mswap. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="70a39-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="70a39-119">**Serialzahldauer**</span><span class="sxs-lookup"><span data-stu-id="70a39-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="70a39-120">Tatsächliche Länge der zurückgegebenen Seriennummer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="70a39-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a39-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70a39-121">Requirements</span></span>



| <span data-ttu-id="70a39-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70a39-122">Requirement</span></span> | <span data-ttu-id="70a39-123">Wert</span><span class="sxs-lookup"><span data-stu-id="70a39-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70a39-124">Header</span><span class="sxs-lookup"><span data-stu-id="70a39-124">Header</span></span><br/> | <dl> <span data-ttu-id="70a39-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70a39-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a39-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70a39-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a39-127">**Imdspdevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="70a39-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="70a39-128">**Imdspstorageglobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="70a39-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="70a39-129">**Iwmdmdevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="70a39-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="70a39-130">**Iwmdmstorageglobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="70a39-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="70a39-131">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="70a39-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





