---
description: Die Drucker \_ Info \_ 7-Struktur gibt Verzeichnisdienst-Drucker Informationen an.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357026"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="0af62-103">Drucker \_ Info \_ 7-Struktur</span><span class="sxs-lookup"><span data-stu-id="0af62-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="0af62-104">Die **Drucker \_ Info \_ 7** -Struktur gibt Verzeichnisdienst-Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="0af62-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="0af62-105">Verwenden Sie diese Struktur mit der [**SetPrinter**](setprinter.md) -Funktion, um die Daten eines Druckers im Verzeichnisdienst (DS) zu veröffentlichen oder um die veröffentlichten Daten eines Druckers aus den DS zu aktualisieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0af62-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="0af62-106">Verwenden Sie diese Struktur mit der [**GetPrinter**](getprinter.md) -Funktion, um zu bestimmen, ob ein Drucker in DS veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="0af62-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af62-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0af62-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="0af62-108">Member</span><span class="sxs-lookup"><span data-stu-id="0af62-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0af62-109">**pszobjectguid**</span><span class="sxs-lookup"><span data-stu-id="0af62-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="0af62-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die GUID des Verzeichnisdienst-Druck Warteschlangen Objekts enthält, das einem veröffentlichten Drucker zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0af62-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="0af62-111">Verwenden Sie die [**GetPrinter**](getprinter.md) -Funktion, um diese GUID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0af62-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="0af62-112">Legen Sie **pszobjectguid** vor dem Aufrufen von [**SetPrinter**](setprinter.md)auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="0af62-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0af62-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="0af62-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="0af62-114">Gibt die Aktion an, die von der [**SetPrinter**](setprinter.md) -Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0af62-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="0af62-115">Bei der [**GetPrinter**](getprinter.md) -Funktion gibt dieser Member an, ob der angegebene Drucker veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="0af62-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="0af62-116">Dieser Member kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="0af62-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="0af62-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0af62-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="0af62-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0af62-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="0af62-119"><dt>**Dsprint \_ Ausstehende**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="0af62-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="0af62-120">[**GetPrinter**](getprinter.md): gibt an, dass das System versucht, einen Vorgang zum Veröffentlichen oder Aufheben der Veröffentlichung auszuführen, der von einem [**SetPrinter**](setprinter.md) -Befehl gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0af62-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="0af62-121">[**SetPrinter**](setprinter.md): dieser Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0af62-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="0af62-122"><dt>**Dsprint \_**</dt> <dt>0x00000001</dt> veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="0af62-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="0af62-123">[**SetPrinter**](setprinter.md): veröffentlicht die Druckerdaten in DS.</span><span class="sxs-lookup"><span data-stu-id="0af62-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="0af62-124">[**GetPrinter**](getprinter.md): gibt an, dass der Drucker veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="0af62-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="0af62-125"><dt>**Dsprint \_**</dt> <dt>0x00000008</dt> erneut veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="0af62-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="0af62-126">[**SetPrinter**](setprinter.md): die DS-Daten für den Drucker werden nicht veröffentlicht und dann erneut veröffentlicht, sodass alle Eigenschaften im veröffentlichten Drucker aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0af62-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="0af62-127">Bei der erneuten Veröffentlichung wird auch die GUID des veröffentlichten Druckers geändert.</span><span class="sxs-lookup"><span data-stu-id="0af62-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="0af62-128">[**GetPrinter**](getprinter.md): gibt diesen Wert nie zurück.</span><span class="sxs-lookup"><span data-stu-id="0af62-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="0af62-129"><dt>**Dsprint \_ Veröffentlichung**</dt> von <dt>0x00000004</dt> aufheben</span><span class="sxs-lookup"><span data-stu-id="0af62-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="0af62-130">[**SetPrinter**](setprinter.md): entfernt die veröffentlichten Daten des Druckers aus dem DS.</span><span class="sxs-lookup"><span data-stu-id="0af62-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="0af62-131">[**GetPrinter**](getprinter.md): gibt an, dass der Drucker nicht veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="0af62-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="0af62-132"><dt>**Dsprint \_**</dt> <dt>0x00000002</dt> aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0af62-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="0af62-133">[**SetPrinter**](setprinter.md): aktualisiert die veröffentlichten Daten des Druckers in DS.</span><span class="sxs-lookup"><span data-stu-id="0af62-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="0af62-134">[**GetPrinter**](getprinter.md): gibt diesen Wert nie zurück.</span><span class="sxs-lookup"><span data-stu-id="0af62-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0af62-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af62-135">Remarks</span></span>

<span data-ttu-id="0af62-136">Die **Drucker \_ Info \_ 7** -Struktur wird in einem [**SetPrinter**](setprinter.md) -Befehl verwendet, um Drucker Informationen im Verzeichnisdienst zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0af62-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="0af62-137">Die veröffentlichten Daten umfassen alle Werte und Daten für den angegebenen Drucker, der sich unter dem \_ spoolerschlüssel (splds Spooler \_ Key, splds \_ Driver Key) befindet \_ , oder die \_ \_ von [**setprinterdataex**](setprinterdataex.md)erstellten Benutzerschlüssel Schlüssel von splds.</span><span class="sxs-lookup"><span data-stu-id="0af62-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="0af62-138">Für [**SetPrinter**](setprinter.md)sollte *pszobjectguid* auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0af62-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="0af62-139">Bei [**GetPrinter**](getprinter.md)gibt *pszobjectguid* die GUID des druckwarteschlangenobjekts der Verzeichnisdienste zurück, das einem veröffentlichten Drucker zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0af62-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="0af62-140">Sie können diese GUID mit ADSI-Methoden (Active Directory Services Interface) verwenden, um veröffentlichte Daten für den Drucker abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0af62-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="0af62-141">Die empfohlene Methode zum Abrufen veröffentlichter Daten ist jedoch das Aufrufen der [**getprinterdataex**](getprinterdataex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0af62-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af62-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0af62-142">Requirements</span></span>



| <span data-ttu-id="0af62-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0af62-143">Requirement</span></span> | <span data-ttu-id="0af62-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0af62-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af62-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0af62-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0af62-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0af62-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0af62-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0af62-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0af62-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0af62-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0af62-149">Header</span><span class="sxs-lookup"><span data-stu-id="0af62-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af62-150"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0af62-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0af62-151">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0af62-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0af62-152">**\_ Drucker \_ Informationen \_ 7W** (Unicode) und **\_ Drucker \_ Info \_ 7a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0af62-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="0af62-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0af62-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af62-154">Drucken</span><span class="sxs-lookup"><span data-stu-id="0af62-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0af62-155">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0af62-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




