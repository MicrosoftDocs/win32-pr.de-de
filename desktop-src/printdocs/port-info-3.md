---
description: Die Port \_ Info \_ 3-Struktur gibt den Statuswert eines Drucker Anschlusses an.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: PORT_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363456"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="46199-103">Port \_ Info \_ 3-Struktur</span><span class="sxs-lookup"><span data-stu-id="46199-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="46199-104">Die **Port \_ Info \_ 3** -Struktur gibt den Statuswert eines Drucker Anschlusses an.</span><span class="sxs-lookup"><span data-stu-id="46199-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="46199-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46199-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="46199-106">Member</span><span class="sxs-lookup"><span data-stu-id="46199-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46199-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="46199-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="46199-108">Der neue Port Statuswert.</span><span class="sxs-lookup"><span data-stu-id="46199-108">The new port status value.</span></span> <span data-ttu-id="46199-109">Dieser Wert wird nur verwendet, wenn der **pszstatus** -Member **null** ist.</span><span class="sxs-lookup"><span data-stu-id="46199-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="46199-110">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="46199-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="46199-111">Wert</span><span class="sxs-lookup"><span data-stu-id="46199-111">Value</span></span>                            | <span data-ttu-id="46199-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="46199-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="46199-113">0</span><span class="sxs-lookup"><span data-stu-id="46199-113">0</span></span>                                | <span data-ttu-id="46199-114">Löscht den Status des Drucker Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="46199-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="46199-115">Port \_ Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="46199-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="46199-116">Der Drucker des Ports ist offline.</span><span class="sxs-lookup"><span data-stu-id="46199-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="46199-117">Port \_ Status \_ Papier \_ Marmelade</span><span class="sxs-lookup"><span data-stu-id="46199-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="46199-118">Der Drucker des Ports hat eine Papier Marmelade.</span><span class="sxs-lookup"><span data-stu-id="46199-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="46199-119">Port \_ Status \_ Papier \_ out</span><span class="sxs-lookup"><span data-stu-id="46199-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="46199-120">Der Drucker des Ports ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="46199-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="46199-121">Port \_ Status- \_ Ausgabe \_ bin \_ voll</span><span class="sxs-lookup"><span data-stu-id="46199-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="46199-122">Der Ausgabe Korb des Ports ist voll.</span><span class="sxs-lookup"><span data-stu-id="46199-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="46199-123">Problem mit dem Port \_ Status \_ Papier \_</span><span class="sxs-lookup"><span data-stu-id="46199-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="46199-124">Der Drucker des Ports hat ein Papier Problem.</span><span class="sxs-lookup"><span data-stu-id="46199-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="46199-125">Port \_ Status \_ kein \_ Toner</span><span class="sxs-lookup"><span data-stu-id="46199-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="46199-126">Der Drucker des Ports ist nicht mehr Toner.</span><span class="sxs-lookup"><span data-stu-id="46199-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="46199-127">Port \_ Status- \_ Tür \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="46199-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="46199-128">Die Tür des Drucker des Ports ist offen.</span><span class="sxs-lookup"><span data-stu-id="46199-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="46199-129">Port \_ Status \_ Benutzer \_ Eingriff</span><span class="sxs-lookup"><span data-stu-id="46199-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="46199-130">Der Drucker des Ports erfordert einen Benutzereingriff.</span><span class="sxs-lookup"><span data-stu-id="46199-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="46199-131">Port \_ Status \_ nicht genügend Arbeits \_ \_ Speicher</span><span class="sxs-lookup"><span data-stu-id="46199-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="46199-132">Der Drucker des Ports weist nicht genügend Arbeitsspeicher auf.</span><span class="sxs-lookup"><span data-stu-id="46199-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="46199-133">Port \_ Status- \_ Toner \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="46199-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="46199-134">Der Drucker des Ports ist auf dem Toner niedrig.</span><span class="sxs-lookup"><span data-stu-id="46199-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="46199-135">\_ \_ Anwärm Status des Ports \_</span><span class="sxs-lookup"><span data-stu-id="46199-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="46199-136">Der Drucker des Ports wird erwärmt.</span><span class="sxs-lookup"><span data-stu-id="46199-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="46199-137">\_ \_ Energiespar Status des Port Status \_</span><span class="sxs-lookup"><span data-stu-id="46199-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="46199-138">Der Drucker des Ports befindet sich in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="46199-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="46199-139">**pszstatus**</span><span class="sxs-lookup"><span data-stu-id="46199-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="46199-140">Zeiger auf eine neue festzulegende Wert Zeichenfolge für den Drucker Anschluss.</span><span class="sxs-lookup"><span data-stu-id="46199-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="46199-141">Verwenden Sie dieses Mitglied, wenn es keinen geeigneten Statuswert für den **dwStatus**-Wert gibt.</span><span class="sxs-lookup"><span data-stu-id="46199-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="46199-142">**dwschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="46199-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="46199-143">Der Schweregrad des Port Status Werts.</span><span class="sxs-lookup"><span data-stu-id="46199-143">The severity of the port status value.</span></span>

<span data-ttu-id="46199-144">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="46199-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="46199-145">Wert</span><span class="sxs-lookup"><span data-stu-id="46199-145">Value</span></span>                       | <span data-ttu-id="46199-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="46199-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="46199-147">\_Fehler beim \_ Porttyp. \_</span><span class="sxs-lookup"><span data-stu-id="46199-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="46199-148">Der Wert für den Port Status weist auf einen Fehler hin.</span><span class="sxs-lookup"><span data-stu-id="46199-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="46199-149">Port \_ Status \_ \_ Warnung</span><span class="sxs-lookup"><span data-stu-id="46199-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="46199-150">Der Wert für den Port Status ist eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="46199-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="46199-151">Informationen zum Port \_ Status- \_ Typ \_</span><span class="sxs-lookup"><span data-stu-id="46199-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="46199-152">Der Port Statuswert ist "Information".</span><span class="sxs-lookup"><span data-stu-id="46199-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46199-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46199-153">Remarks</span></span>

<span data-ttu-id="46199-154">Wenn Sie einen druckerportstatuswert mit dem Wert " \_ \_ Fehler beim Porttyp" festlegen \_ , beendet der Druck Spooler das Senden von Aufträgen an den Port.</span><span class="sxs-lookup"><span data-stu-id="46199-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="46199-155">Der Druck Spooler setzt das Senden von Aufträgen an den Port erst fort, wenn ein anderer [**setPort**](setport.md) -Rückruf zum Löschen des Status erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="46199-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="46199-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46199-156">Requirements</span></span>



| <span data-ttu-id="46199-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46199-157">Requirement</span></span> | <span data-ttu-id="46199-158">Wert</span><span class="sxs-lookup"><span data-stu-id="46199-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46199-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46199-159">Minimum supported client</span></span><br/> | <span data-ttu-id="46199-160">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46199-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46199-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46199-161">Minimum supported server</span></span><br/> | <span data-ttu-id="46199-162">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46199-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46199-163">Header</span><span class="sxs-lookup"><span data-stu-id="46199-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="46199-164"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46199-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="46199-165">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="46199-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46199-166">**\_ Port \_ Info \_ 3W** (Unicode) und **\_ Port \_ Info \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="46199-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="46199-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46199-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46199-168">Drucken</span><span class="sxs-lookup"><span data-stu-id="46199-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="46199-169">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="46199-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="46199-170">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="46199-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




