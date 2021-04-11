---
description: Gibt das Caching eines Handles für einen mit OpenPrinter2 geöffneten Drucker an.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS-Enumeration (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217538"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="9ad01-103">\_Druckeroptionsflags- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="9ad01-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="9ad01-104">Gibt das Caching eines Handles für einen mit [**OpenPrinter2**](openprinter2.md)geöffneten Drucker an.</span><span class="sxs-lookup"><span data-stu-id="9ad01-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad01-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="9ad01-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9ad01-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9ad01-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**Drucker \_ Option " \_ kein \_ Cache"**</span><span class="sxs-lookup"><span data-stu-id="9ad01-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="9ad01-108">Das Handle wird nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9ad01-108">The handle is not cached.</span></span> <span data-ttu-id="9ad01-109">Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurück gegebenes handle angewendet werden, werden auf den Remote Computer übertragen.</span><span class="sxs-lookup"><span data-stu-id="9ad01-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="9ad01-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**Drucker \_ options \_ Cache**</span><span class="sxs-lookup"><span data-stu-id="9ad01-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="9ad01-111">Das Handle wird zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9ad01-111">The handle is cached.</span></span> <span data-ttu-id="9ad01-112">Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurück gegebenes handle angewendet werden, werden in den lokalen Cache übertragen.</span><span class="sxs-lookup"><span data-stu-id="9ad01-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="9ad01-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**Drucker \_ Option \_ Client \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="9ad01-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="9ad01-114">Das von [**OpenPrinter2**](openprinter2.md) zurückgegebene Handle kann von [**SetPrinter**](setprinter.md) zum Umbenennen der Druckerverbindung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ad01-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ad01-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ad01-115">Requirements</span></span>



| <span data-ttu-id="9ad01-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ad01-116">Requirement</span></span> | <span data-ttu-id="9ad01-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9ad01-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad01-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ad01-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad01-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ad01-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9ad01-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ad01-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad01-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ad01-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ad01-122">Header</span><span class="sxs-lookup"><span data-stu-id="9ad01-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ad01-123"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad01-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad01-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ad01-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad01-125">Drucken</span><span class="sxs-lookup"><span data-stu-id="9ad01-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9ad01-126">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9ad01-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9ad01-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="9ad01-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="9ad01-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9ad01-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




