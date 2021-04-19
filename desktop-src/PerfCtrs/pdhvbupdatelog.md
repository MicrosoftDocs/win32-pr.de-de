---
description: Die Funktion pdhvbupdatelog Functions aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei. Diese Funktion ruft pdhupdatelog auf.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Pdhvbupdatelog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349221"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="6cf09-104">Pdhvbupdatelog-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="6cf09-105">Die Funktion **pdhvbupdatelog** Functions aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="6cf09-106">Diese Funktion ruft [**pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)auf.</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cf09-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6cf09-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="6cf09-109">Funktion pdhvbupdatelog ( \_ ByVal hlog as PDH \_ hlog, \_ ByVal szuserstring as LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="6cf09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf09-111">*hlog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf09-112">Handle für die zu Aktualisier Ende Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="6cf09-113">Dieses Handle wird von der [**pdhvbopenlog**](pdhvbopenlog.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6cf09-114">*szuserstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf09-115">Ein Zeiger auf eine Zeichenfolge, die die Daten angibt, die der Protokolldatei hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="6cf09-116">Dies wird im Allgemeinen für Kommentare in der Protokolldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cf09-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf09-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cf09-117">Return value</span></span>

<span data-ttu-id="6cf09-118">Wenn die Funktion erfolgreich ausgeführt wird, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf09-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="6cf09-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6cf09-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="6cf09-120">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="6cf09-120">The following are possible values.</span></span>



| <span data-ttu-id="6cf09-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6cf09-121">Return code</span></span>                                                                                                | <span data-ttu-id="6cf09-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cf09-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cf09-123"><dt>**nicht genügend PDH- \_ \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="6cf09-124">Die angeforderten Daten sind größer als der angegebene Puffer.</span><span class="sxs-lookup"><span data-stu-id="6cf09-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="6cf09-125">Die angeforderten Daten können nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6cf09-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="6cf09-126"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="6cf09-127">Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.</span><span class="sxs-lookup"><span data-stu-id="6cf09-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="6cf09-128"><dt>**Ungültiges PDH- \_ \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="6cf09-129">Das Handle ist kein gültiges PDH-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6cf09-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6cf09-130"><dt>**Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="6cf09-131">Die angegebene Protokolldatei kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6cf09-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6cf09-132"><dt>**PDH- \_ Datei wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="6cf09-133">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6cf09-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="6cf09-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cf09-134">Remarks</span></span>

<span data-ttu-id="6cf09-135">Es muss eine aktuell geöffnete Abfrage vorhanden sein, und die gewünschten Zähler müssen hinzugefügt werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cf09-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf09-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cf09-136">Requirements</span></span>



| <span data-ttu-id="6cf09-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cf09-137">Requirement</span></span> | <span data-ttu-id="6cf09-138">Wert</span><span class="sxs-lookup"><span data-stu-id="6cf09-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf09-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cf09-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf09-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cf09-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cf09-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cf09-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf09-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cf09-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6cf09-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6cf09-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cf09-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="6cf09-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf09-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf09-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf09-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf09-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cf09-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf09-148">**Pdhupdatelog**</span><span class="sxs-lookup"><span data-stu-id="6cf09-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="6cf09-149">**Pdhvbgetlogfilesize**</span><span class="sxs-lookup"><span data-stu-id="6cf09-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="6cf09-150">**Pdhvbopenlog**</span><span class="sxs-lookup"><span data-stu-id="6cf09-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

