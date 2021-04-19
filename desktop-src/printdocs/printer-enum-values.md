---
description: Die \_ Struktur der druckeraufgabenwerte \_ gibt den Wert Namen, den Typ und die Daten für einen von der enumprinterdataex-Funktion zurückgegebenen Drucker Konfigurations Wert an.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: PRINTER_ENUM_VALUES Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362310"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="1c005-103">Struktur der druckerenumerationswerte \_ \_</span><span class="sxs-lookup"><span data-stu-id="1c005-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="1c005-104">Die Struktur der **druckeraufgabenwerte \_ \_** gibt den Wert Namen, den Typ und die Daten für einen von der [**enumprinterdataex**](enumprinterdataex.md) -Funktion zurückgegebenen Drucker Konfigurations Wert an.</span><span class="sxs-lookup"><span data-stu-id="1c005-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c005-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c005-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="1c005-106">Member</span><span class="sxs-lookup"><span data-stu-id="1c005-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1c005-107">**pvaluename**</span><span class="sxs-lookup"><span data-stu-id="1c005-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="1c005-108">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des abgerufenen Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="1c005-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="1c005-109">**cbvaluename**</span><span class="sxs-lookup"><span data-stu-id="1c005-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="1c005-110">Die Anzahl der Bytes im **pvaluename** -Member, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1c005-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="1c005-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="1c005-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="1c005-112">Ein Code, der den Typ der Daten angibt, auf die der **pData** -Member verweist.</span><span class="sxs-lookup"><span data-stu-id="1c005-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="1c005-113">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="1c005-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="1c005-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="1c005-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="1c005-115">Zeiger auf einen Puffer, der die Daten für den abgerufenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="1c005-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="1c005-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="1c005-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="1c005-117">Die Anzahl von Bytes, die im **pData** -Puffer abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="1c005-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c005-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c005-118">Requirements</span></span>



| <span data-ttu-id="1c005-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c005-119">Requirement</span></span> | <span data-ttu-id="1c005-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1c005-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c005-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c005-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c005-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c005-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1c005-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c005-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c005-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c005-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1c005-125">Header</span><span class="sxs-lookup"><span data-stu-id="1c005-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c005-126"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c005-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1c005-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="1c005-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1c005-128">**\_ \_ Druckerenum \_ valuesw** (Unicode) und **\_ Printer \_ Enum \_ valuesa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1c005-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1c005-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c005-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c005-130">Drucken</span><span class="sxs-lookup"><span data-stu-id="1c005-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1c005-131">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1c005-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1c005-132">**Enumprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="1c005-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

