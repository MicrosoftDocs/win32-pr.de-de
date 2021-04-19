---
description: Stellt Druckeroptionen dar.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: PRINTER_OPTIONS Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362535"
---
# <a name="printer_options-structure"></a><span data-ttu-id="edbc0-103">Struktur der Drucker \_ Optionen</span><span class="sxs-lookup"><span data-stu-id="edbc0-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="edbc0-104">Stellt Druckeroptionen dar.</span><span class="sxs-lookup"><span data-stu-id="edbc0-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbc0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edbc0-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="edbc0-106">Member</span><span class="sxs-lookup"><span data-stu-id="edbc0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="edbc0-107">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="edbc0-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="edbc0-108">Die Größe der **Drucker \_ options** Struktur.</span><span class="sxs-lookup"><span data-stu-id="edbc0-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="edbc0-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="edbc0-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="edbc0-110">Ein Satz von [**\_ druckeroptionsflags \_**](printer-option-flags.md) , der angibt, wie das Handle für einen Drucker, der von [**OpenPrinter2**](openprinter2.md) zurückgegeben wird, von anderen Funktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="edbc0-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edbc0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edbc0-111">Requirements</span></span>



| <span data-ttu-id="edbc0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edbc0-112">Requirement</span></span> | <span data-ttu-id="edbc0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="edbc0-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbc0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edbc0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="edbc0-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edbc0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="edbc0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edbc0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="edbc0-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edbc0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="edbc0-118">Header</span><span class="sxs-lookup"><span data-stu-id="edbc0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbc0-119"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edbc0-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbc0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edbc0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbc0-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="edbc0-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="edbc0-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="edbc0-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="edbc0-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="edbc0-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="edbc0-124">**\_druckeroptionsflags \_**</span><span class="sxs-lookup"><span data-stu-id="edbc0-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




