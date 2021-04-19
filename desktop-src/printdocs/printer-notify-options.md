---
description: Die Struktur der Drucker \_ \_ Benachrichtigungs Optionen gibt Optionen für ein Änderungs Benachrichtigungs Objekt an, das einen Drucker oder Druckserver überwacht.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362294"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="acdb2-103">Struktur der Drucker \_ Benachrichtigungs \_ Optionen</span><span class="sxs-lookup"><span data-stu-id="acdb2-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="acdb2-104">Die Struktur der **Drucker \_ Benachrichtigungs \_ Optionen** gibt Optionen für ein Änderungs Benachrichtigungs Objekt an, das einen Drucker oder Druckserver überwacht.</span><span class="sxs-lookup"><span data-stu-id="acdb2-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="acdb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acdb2-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="acdb2-106">Member</span><span class="sxs-lookup"><span data-stu-id="acdb2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="acdb2-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="acdb2-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="acdb2-108">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="acdb2-108">The version of this structure.</span></span> <span data-ttu-id="acdb2-109">Legen Sie diesen Member auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="acdb2-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="acdb2-110">**Flags**</span><span class="sxs-lookup"><span data-stu-id="acdb2-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="acdb2-111">Ein Bitflag.</span><span class="sxs-lookup"><span data-stu-id="acdb2-111">A bit flag.</span></span> <span data-ttu-id="acdb2-112">Wenn Sie \_ \_ in einem aufzurufenden Befehl die Funktion " \_ [**findnextprinterchangenotifi"**](findnextprinterchangenotification.md) das Aktualisierungs Flag für Drucker Benachrichtigen festlegen, stellt die Funktion aktuelle Daten für alle überwachten Drucker Informationsfelder bereit.</span><span class="sxs-lookup"><span data-stu-id="acdb2-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="acdb2-113">Die [**findfirstprinterchangenotifi-**](findfirstprinterchangenotification.md) Funktion ignoriert den **Flags** -Member.</span><span class="sxs-lookup"><span data-stu-id="acdb2-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="acdb2-114">**Count**</span><span class="sxs-lookup"><span data-stu-id="acdb2-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="acdb2-115">Die Anzahl der Elemente im **ptypes** -Array.</span><span class="sxs-lookup"><span data-stu-id="acdb2-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="acdb2-116">**ptypes**</span><span class="sxs-lookup"><span data-stu-id="acdb2-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="acdb2-117">Ein Zeiger auf ein Array von [**Optionen für den \_ druckerbenachrichtigungs- \_ \_ Typ**](printer-notify-options-type.md) .</span><span class="sxs-lookup"><span data-stu-id="acdb2-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="acdb2-118">Verwenden Sie ein Element dieses Arrays, um die zu überwachenden Drucker Informationsfelder anzugeben, und ein Element, um die zu überwachenden Felder der Auftrags Informationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="acdb2-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="acdb2-119">Sie können entweder Drucker Informationen, Auftrags Informationen oder beides überwachen.</span><span class="sxs-lookup"><span data-stu-id="acdb2-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acdb2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acdb2-120">Remarks</span></span>

<span data-ttu-id="acdb2-121">Verwenden Sie diese Struktur mit der [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) , um die Gruppe der Drucker-oder Auftrags Informationsfelder anzugeben, die auf Änderungen überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="acdb2-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="acdb2-122">Verwenden Sie diese Struktur mit der [**findnextprinterchangenotifizierungsfunktion**](findnextprinterchangenotification.md) , um die aktuellen Daten für alle überwachten Drucker-und Auftrags Informationsfelder anzufordern.</span><span class="sxs-lookup"><span data-stu-id="acdb2-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="acdb2-123">In diesem Fall gibt das **Flags** -Element das \_ Aktualisierungs Flag für Drucker Benachrichtigungen an \_ \_ , und die Funktion ignoriert die anderen Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="acdb2-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="acdb2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acdb2-124">Requirements</span></span>



| <span data-ttu-id="acdb2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acdb2-125">Requirement</span></span> | <span data-ttu-id="acdb2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="acdb2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdb2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acdb2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="acdb2-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acdb2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="acdb2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acdb2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="acdb2-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acdb2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="acdb2-131">Header</span><span class="sxs-lookup"><span data-stu-id="acdb2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="acdb2-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acdb2-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acdb2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acdb2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acdb2-134">Drucken</span><span class="sxs-lookup"><span data-stu-id="acdb2-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="acdb2-135">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="acdb2-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="acdb2-136">**Findfirstprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="acdb2-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="acdb2-137">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="acdb2-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="acdb2-138">**Typ der Drucker \_ Benachrichtigungs \_ Optionen \_**</span><span class="sxs-lookup"><span data-stu-id="acdb2-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




