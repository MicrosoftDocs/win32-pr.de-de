---
description: Die Drucker \_ Info \_ 3-Struktur gibt Drucker Sicherheitsinformationen an.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: PRINTER_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360725"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="4df35-103">Drucker \_ Info \_ 3-Struktur</span><span class="sxs-lookup"><span data-stu-id="4df35-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="4df35-104">Die **Drucker \_ Info \_ 3** -Struktur gibt Drucker Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4df35-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df35-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="4df35-106">Member</span><span class="sxs-lookup"><span data-stu-id="4df35-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4df35-107">**psecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="4df35-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="4df35-108">Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die die Sicherheitsinformationen eines Druckers angibt.</span><span class="sxs-lookup"><span data-stu-id="4df35-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4df35-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df35-109">Remarks</span></span>

<span data-ttu-id="4df35-110">Die **Drucker \_ Info \_ 3** -Struktur ermöglicht es einer Anwendung, die Sicherheits Beschreibung eines Druckers zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4df35-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="4df35-111">Der Aufrufer kann dies auch dann tun, wenn ihm bestimmte Drucker Berechtigungen fehlen, sofern er über die in " [**SetPrinter**](setprinter.md) " und " [**GetPrinter**](getprinter.md)" beschriebenen Standardrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="4df35-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="4df35-112">Folglich kann eine Anwendung vorübergehend den gesamten Zugriff auf einen Drucker verweigern, während der Besitzer des Druckers auf die freigegebene ACL des Druckers zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4df35-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df35-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4df35-113">Requirements</span></span>



| <span data-ttu-id="4df35-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4df35-114">Requirement</span></span> | <span data-ttu-id="4df35-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4df35-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df35-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4df35-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4df35-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df35-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4df35-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4df35-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4df35-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df35-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4df35-120">Header</span><span class="sxs-lookup"><span data-stu-id="4df35-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df35-121"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4df35-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df35-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4df35-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df35-123">Drucken</span><span class="sxs-lookup"><span data-stu-id="4df35-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4df35-124">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4df35-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4df35-125">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4df35-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="4df35-126">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4df35-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="4df35-127">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4df35-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="4df35-128">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4df35-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="4df35-129">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4df35-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="4df35-130">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4df35-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

