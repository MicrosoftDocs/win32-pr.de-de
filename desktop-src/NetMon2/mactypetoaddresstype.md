---
description: Die Funktion "mactypedeadresssstype" konvertiert einen angegebenen Mac-Typ in einen Adresstyp.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Mactypedeadresssstype-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862859"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="7c3a0-103">Mactypedeadresssstype-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c3a0-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="7c3a0-104">Die Funktion " **mactypedeadresssstype** " konvertiert einen angegebenen Mac-Typ in einen Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c3a0-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="7c3a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c3a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3a0-107">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c3a0-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3a0-108">Der Mac-Typ, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-108">MAC type to be converted.</span></span> <span data-ttu-id="7c3a0-109">Geben Sie einen der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-109">Specify one of the following values:</span></span>

<span data-ttu-id="7c3a0-110">Mac \_ Type \_ Ethernet Mac \_ Type \_ TokenRing Mac \_ Type \_ f</span><span class="sxs-lookup"><span data-stu-id="7c3a0-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3a0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c3a0-111">Return value</span></span>

<span data-ttu-id="7c3a0-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="7c3a0-113">Address \_ Type \_ Ethernet Address \_ Type \_ TokenRing Address \_ Type \_ f</span><span class="sxs-lookup"><span data-stu-id="7c3a0-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="7c3a0-114">Wenn die Funktion nicht erfolgreich ist, ist der Mac-Typ unbekannt. der Rückgabewert ist-1.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c3a0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c3a0-115">Remarks</span></span>

<span data-ttu-id="7c3a0-116">[*Experten*](e.md) und [*Parser*](p.md) können die Funktion " **mactypedeadresssstype** " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7c3a0-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3a0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c3a0-117">Requirements</span></span>



| <span data-ttu-id="7c3a0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c3a0-118">Requirement</span></span> | <span data-ttu-id="7c3a0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7c3a0-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3a0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c3a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3a0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c3a0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7c3a0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c3a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3a0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c3a0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7c3a0-124">Header</span><span class="sxs-lookup"><span data-stu-id="7c3a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3a0-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a0-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7c3a0-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c3a0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c3a0-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a0-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c3a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3a0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c3a0-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a0-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




