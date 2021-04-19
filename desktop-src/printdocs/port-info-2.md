---
description: Die \_ Struktur Port Info \_ 2 identifiziert einen unterstützten Druckerport.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349332"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="b0fbd-103">Port \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="b0fbd-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="b0fbd-104">Die Struktur **Port \_ Info \_ 2** identifiziert einen unterstützten Druckerport.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0fbd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0fbd-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="b0fbd-106">Member</span><span class="sxs-lookup"><span data-stu-id="b0fbd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0fbd-107">**pportname**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="b0fbd-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen unterstützten Druckerport identifiziert (z. b. "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="b0fbd-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="b0fbd-109">**pmonitorname**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="b0fbd-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen installierten Monitor identifiziert (z. b. "PJL-Monitor").</span><span class="sxs-lookup"><span data-stu-id="b0fbd-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="b0fbd-111">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0fbd-112">**pdescription**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="b0fbd-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Port ausführlicher beschreibt (z. b. wenn " **pportname** " den Wert "LPT1:" hat, " **pdescription** " ist "Printer Port").</span><span class="sxs-lookup"><span data-stu-id="b0fbd-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="b0fbd-114">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0fbd-115">**"f"**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="b0fbd-116">Bitmaske, die den Porttyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="b0fbd-117">Dieser Member kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="b0fbd-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="b0fbd-118">**\_Porttyp \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="b0fbd-119">**\_Porttyp \_ Lesen**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="b0fbd-120">**\_umgeleitete Porttyp \_**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="b0fbd-121">**\_Porttyp \_ Netzwerk \_ angefügt**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b0fbd-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b0fbd-123">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0fbd-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0fbd-124">Remarks</span></span>

<span data-ttu-id="b0fbd-125">Verwenden Sie die **Port \_ Info \_ 2** -Struktur beim Aufrufen von [**enumports**](enumports.md) , wenn mehrere Monitore installiert sind, die die gleichen Ports unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="b0fbd-126">Der **fporttype** -Member kann abgefragt werden, um Informationen über den Port zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b0fbd-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="b0fbd-127">Beachten Sie, dass die Port Einstellungen keine Drucker Attribute beeinflussen (wie vom **Attribute** -Member von [**Printer \_ Info \_ 2**](printer-info-2.md)zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="b0fbd-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fbd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0fbd-128">Requirements</span></span>



| <span data-ttu-id="b0fbd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0fbd-129">Requirement</span></span> | <span data-ttu-id="b0fbd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b0fbd-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0fbd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fbd-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0fbd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0fbd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0fbd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fbd-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0fbd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0fbd-135">Header</span><span class="sxs-lookup"><span data-stu-id="b0fbd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fbd-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbd-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b0fbd-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b0fbd-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0fbd-138">**\_ Port \_ Info \_ 2W** (Unicode) und **\_ Port \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0fbd-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="b0fbd-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0fbd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fbd-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="b0fbd-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b0fbd-141">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b0fbd-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b0fbd-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="b0fbd-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




