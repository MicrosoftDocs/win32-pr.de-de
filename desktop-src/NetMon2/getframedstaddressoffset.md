---
description: Die getframedstaddressoffset-Funktion gibt den Offset an die Zieladresse eines angegebenen Frames zurück.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Getframedstaddressoffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345660"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="f65f6-103">Getframedstaddressoffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="f65f6-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="f65f6-104">Die **getframedstaddressoffset** -Funktion gibt den Offset an die Zieladresse eines angegebenen Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="f65f6-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f65f6-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="f65f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f65f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65f6-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f65f6-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65f6-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="f65f6-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f65f6-109">*Adresstype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f65f6-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65f6-110">Der Typ der Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="f65f6-110">Type of the destination address.</span></span> <span data-ttu-id="f65f6-111">Geben Sie einen der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="f65f6-111">Specify one of the following values:</span></span>

<span data-ttu-id="f65f6-112">Address \_ Type \_ Ethernet Address \_ Type \_ IP Address Type IP Address Type IP Address Type \_ \_ IPX Address \_ Type \_ TokenRing Address Type Typ des Typs " \_ \_ XNS Address Type" der \_ \_ \_ \_ \_ IP-Adresse \_ \_ des Typs "ATM".</span><span class="sxs-lookup"><span data-stu-id="f65f6-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="f65f6-113">*Addresslength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f65f6-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65f6-114">Länge der Zieladresse in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f65f6-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65f6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f65f6-115">Return value</span></span>

<span data-ttu-id="f65f6-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset (in Bytes) bis zum angeforderten Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="f65f6-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="f65f6-117">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).</span><span class="sxs-lookup"><span data-stu-id="f65f6-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="f65f6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f65f6-118">Remarks</span></span>

<span data-ttu-id="f65f6-119">Wenn der *Adresstype* -Parameter auf Address Type Ethernet festgelegt ist \_ \_ , ist der Rückgabewert der **getframedstaddressoffset** -Funktion immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f65f6-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="f65f6-120">Der Offset einer Ethernet-Adresse ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f65f6-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="f65f6-121">[*Experten*](e.md) und [*Parser*](p.md) können die **getframedstaddressoffset** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f65f6-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f65f6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f65f6-122">Requirements</span></span>



| <span data-ttu-id="f65f6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f65f6-123">Requirement</span></span> | <span data-ttu-id="f65f6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f65f6-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f65f6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f65f6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f65f6-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f65f6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f65f6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f65f6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f65f6-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f65f6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f65f6-129">Header</span><span class="sxs-lookup"><span data-stu-id="f65f6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f65f6-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f65f6-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f65f6-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f65f6-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f65f6-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f65f6-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f65f6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f65f6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f65f6-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f65f6-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




