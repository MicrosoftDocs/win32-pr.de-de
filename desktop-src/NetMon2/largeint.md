---
description: Der largeint-Datentyp definiert einen großen \_ ganzzahligen Wert.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: Largeint (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345940"
---
# <a name="largeint"></a><span data-ttu-id="1489c-103">' Largeint</span><span class="sxs-lookup"><span data-stu-id="1489c-103">LARGEINT</span></span>

<span data-ttu-id="1489c-104">Der **largeint** -Datentyp definiert einen [**großen \_ ganzzahligen**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) Wert.</span><span class="sxs-lookup"><span data-stu-id="1489c-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="1489c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1489c-105">Remarks</span></span>

<span data-ttu-id="1489c-106">Der **lplargein-** Member der [**set**](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die einen oder mehrere largeint-Werte definieren.</span><span class="sxs-lookup"><span data-stu-id="1489c-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="1489c-107">Wenn diese Art von **Set** -Struktur angegeben ist, zeigt Netzwerkmonitor eine der folgenden Bezeichnungen mit jedem largeint-Wert an, der im Protokoll Paket gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1489c-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="1489c-108">Entspricht dem Satz Wert.</span><span class="sxs-lookup"><span data-stu-id="1489c-108">Matches set value.</span></span> <span data-ttu-id="1489c-109">Der largeint-Wert ist im Satz enthalten.</span><span class="sxs-lookup"><span data-stu-id="1489c-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="1489c-110">Unbekannter festgelegtem Wert.</span><span class="sxs-lookup"><span data-stu-id="1489c-110">Unknown set value.</span></span> <span data-ttu-id="1489c-111">Der largeint-Wert ist nicht in der Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="1489c-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1489c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1489c-112">Requirements</span></span>



| <span data-ttu-id="1489c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1489c-113">Requirement</span></span> | <span data-ttu-id="1489c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1489c-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1489c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1489c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1489c-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1489c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1489c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1489c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1489c-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1489c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1489c-119">Header</span><span class="sxs-lookup"><span data-stu-id="1489c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1489c-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1489c-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1489c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1489c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1489c-122">SET</span><span class="sxs-lookup"><span data-stu-id="1489c-122">SET</span></span>](set.md)
</dt> </dl>

 

