---
description: Die \_ Typstruktur der druckerbenachrichtigungsoptionen \_ \_ gibt den Satz von Druckern oder Auftrags Informationsfeldern an, die von einem Benachrichtigungs Objekt für Drucker Änderungen überwacht werden sollen. Ein aufzurufende "findfirstprinterchangenotifi"-Funktion gibt eine Drucker \_ Benachrichtigungs \_ Optionen-Struktur an, die ein Array von Optionen für die \_ \_ Typstrukturen der Drucker Benachrichtigung enthält \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: PRINTER_NOTIFY_OPTIONS_TYPE Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353534"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="a7525-103">Drucker \_ Benachrichtigungs \_ Optionen \_ Typstruktur</span><span class="sxs-lookup"><span data-stu-id="a7525-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="a7525-104">Die **\_ \_ \_ Typstruktur der druckerbenachrichtigungsoptionen** gibt den Satz von Druckern oder Auftrags Informationsfeldern an, die von einem Benachrichtigungs Objekt für Drucker Änderungen überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7525-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="a7525-105">Ein aufzurufende " [**findfirstprinterchangenotifi"**](findfirstprinterchangenotification.md) -Funktion gibt eine [**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md) -Struktur an, die ein Array von Optionen für die **\_ \_ \_ Typstrukturen der Drucker Benachrichtigung** enthält.</span><span class="sxs-lookup"><span data-stu-id="a7525-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7525-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7525-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="a7525-107">Member</span><span class="sxs-lookup"><span data-stu-id="a7525-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7525-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="a7525-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-109">Der Typ, der überwacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7525-109">The type to be watched.</span></span> <span data-ttu-id="a7525-110">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a7525-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="a7525-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a7525-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="a7525-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a7525-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="a7525-113"><dt>**Auftrag \_ Benachrichtigen von \_ Typ**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="a7525-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="a7525-114">Gibt an, dass die im **pfields** -Array angegebenen Felder Auftrags \_ Benachrichtigungs \_ Feld \_ \* Konstanten sind.</span><span class="sxs-lookup"><span data-stu-id="a7525-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="a7525-115"><dt>**Drucker \_ Benachrichtigen von \_ Typ**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="a7525-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="a7525-116">Gibt an, dass die im **pfields** -Array angegebenen Felder Drucker \_ Benachrichtigungs \_ Feld \_ \* Konstanten sind.</span><span class="sxs-lookup"><span data-stu-id="a7525-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a7525-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="a7525-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7525-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7525-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="a7525-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7525-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7525-121">**"Reserved2"**</span><span class="sxs-lookup"><span data-stu-id="a7525-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7525-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7525-123">**Count**</span><span class="sxs-lookup"><span data-stu-id="a7525-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-124">Die Anzahl der Elemente im **pfields** -Array.</span><span class="sxs-lookup"><span data-stu-id="a7525-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="a7525-125">**pfields**</span><span class="sxs-lookup"><span data-stu-id="a7525-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="a7525-126">Ein Zeiger auf ein Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="a7525-126">A pointer to an array of values.</span></span> <span data-ttu-id="a7525-127">Jedes Element des Arrays gibt das gewünschte Feld für Aufträge oder Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="a7525-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="a7525-128">Eine Liste der unterstützten Felder für Drucker und Auftrags Informationen finden Sie in der [**\_ \_ \_ Daten**](printer-notify-info-data.md) Struktur zum Benachrichtigen von Drucker Informationen.</span><span class="sxs-lookup"><span data-stu-id="a7525-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7525-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7525-129">Requirements</span></span>



| <span data-ttu-id="a7525-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7525-130">Requirement</span></span> | <span data-ttu-id="a7525-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a7525-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7525-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7525-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a7525-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7525-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7525-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7525-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a7525-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7525-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7525-136">Header</span><span class="sxs-lookup"><span data-stu-id="a7525-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7525-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7525-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7525-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7525-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7525-139">Drucken</span><span class="sxs-lookup"><span data-stu-id="a7525-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a7525-140">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a7525-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a7525-141">**Findfirstprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="a7525-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="a7525-142">**\_ \_ Info \_ Daten für Drucker Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="a7525-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="a7525-143">**Drucker \_ Benachrichtigungs \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="a7525-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




