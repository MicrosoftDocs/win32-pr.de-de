---
description: Die Drucker \_ Benachrichtigungs \_ Struktur enthält Drucker Informationen, die von der findnextprinterchangenotifi-Funktion zurückgegeben werden. Die Funktion gibt diese Informationen zurück, nachdem ein warte Vorgang für ein Benachrichtigungs Objekt für Drucker Änderungen abgeschlossen wurde.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348668"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="2c825-104">Drucker \_ Benachrichtigungs \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="2c825-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="2c825-105">Die **Drucker \_ Benachrichtigungs \_** Struktur enthält Drucker Informationen, die von der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c825-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="2c825-106">Die Funktion gibt diese Informationen zurück, nachdem ein warte Vorgang für ein Benachrichtigungs Objekt für Drucker Änderungen abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2c825-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c825-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c825-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="2c825-108">Member</span><span class="sxs-lookup"><span data-stu-id="2c825-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c825-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="2c825-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2c825-110">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2c825-110">The version of this structure.</span></span> <span data-ttu-id="2c825-111">Legen Sie diesen Member auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="2c825-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="2c825-112">**Flags**</span><span class="sxs-lookup"><span data-stu-id="2c825-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2c825-113">Ein Bitflag, das den Zustand der Benachrichtigungs Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="2c825-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="2c825-114">Wenn das \_ \_ \_ verworfene Bit der Drucker Benachrichtigung festgelegt ist, weist dies darauf hin, dass einige Benachrichtigungen verworfen werden mussten.</span><span class="sxs-lookup"><span data-stu-id="2c825-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="2c825-115">**Count**</span><span class="sxs-lookup"><span data-stu-id="2c825-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="2c825-116">Die Anzahl der [**Drucker \_ Benachrichtigungs \_ \_ Daten**](printer-notify-info-data.md) Elemente im **ADATA** -Array.</span><span class="sxs-lookup"><span data-stu-id="2c825-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="2c825-117">**ADATA**</span><span class="sxs-lookup"><span data-stu-id="2c825-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="2c825-118">Ein Array von [**Drucker \_ \_ Informationen- \_ Daten**](printer-notify-info-data.md) Strukturen, die benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c825-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="2c825-119">Jedes Element des Arrays identifiziert ein einzelnes Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.</span><span class="sxs-lookup"><span data-stu-id="2c825-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c825-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c825-120">Remarks</span></span>

<span data-ttu-id="2c825-121">Wenn für den **Flags** -Member der Wert für das \_ verworfene druckerbenachrichtigungs \_ \_ -Bit festgelegt ist, weist dies darauf hin, dass ein Überlauf oder Fehler aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="2c825-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="2c825-122">In diesem Fall müssen Sie " [**findnextprinterchangenotifi"**](findnextprinterchangenotification.md) aufrufen und das \_ \_ Aktualisierungs Flag für Drucker Benachrichtigungs Optionen angeben \_ , um alle aktuellen Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2c825-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="2c825-123">Bis Sie diesen Aktualisierungs Vorgang anfordern, sendet das System keine weiteren Benachrichtigungen für dieses Änderungs Benachrichtigungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c825-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c825-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c825-124">Requirements</span></span>



| <span data-ttu-id="2c825-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c825-125">Requirement</span></span> | <span data-ttu-id="2c825-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c825-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c825-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c825-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c825-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c825-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c825-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c825-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c825-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c825-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2c825-131">Header</span><span class="sxs-lookup"><span data-stu-id="2c825-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c825-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c825-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c825-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c825-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c825-134">Drucken</span><span class="sxs-lookup"><span data-stu-id="2c825-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2c825-135">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2c825-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2c825-136">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="2c825-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="2c825-137">**\_ \_ Info \_ Daten für Drucker Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="2c825-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 




