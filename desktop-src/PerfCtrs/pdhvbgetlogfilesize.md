---
description: Die pdhvbgetlogfilesize-Funktion gibt die Größe der angegebenen Protokolldatei zurück. Diese Funktion ruft pdhgetlogfilesize auf.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Pdhvbgetlogfilesize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359045"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="13568-104">Pdhvbgetlogfilesize-Funktion</span><span class="sxs-lookup"><span data-stu-id="13568-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="13568-105">Die **pdhvbgetlogfilesize** -Funktion gibt die Größe der angegebenen Protokolldatei zurück.</span><span class="sxs-lookup"><span data-stu-id="13568-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="13568-106">Diese Funktion ruft [**pdhgetlogfilesize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)auf.</span><span class="sxs-lookup"><span data-stu-id="13568-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13568-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="13568-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="13568-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="13568-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="13568-109">Funktion "pdhvbgetlogfilesize" ( \_ ByVal hlog as PDH \_ hlog, \_ ByRef llsize als Long \_ ) als DWORD</span><span class="sxs-lookup"><span data-stu-id="13568-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="13568-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13568-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13568-111">*hlog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13568-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13568-112">Handle für die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="13568-112">Handle to the log file.</span></span> <span data-ttu-id="13568-113">Dieses Handle wird von der [**pdhopenlog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13568-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="13568-114">*llsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13568-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13568-115">Ein Zeiger auf eine Variable, die die Größe der Protokolldatei (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="13568-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13568-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13568-116">Return value</span></span>

<span data-ttu-id="13568-117">Wenn die Funktion erfolgreich ausgeführt wird, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13568-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="13568-118">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="13568-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="13568-119">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="13568-119">The following are possible values.</span></span>



| <span data-ttu-id="13568-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="13568-120">Return code</span></span>                                                                                                | <span data-ttu-id="13568-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13568-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13568-122"><dt>**nicht genügend PDH- \_ \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="13568-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="13568-123">Die angeforderten Daten sind größer als der angegebene Puffer.</span><span class="sxs-lookup"><span data-stu-id="13568-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="13568-124">Die angeforderten Daten können nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="13568-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="13568-125"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="13568-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="13568-126">Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.</span><span class="sxs-lookup"><span data-stu-id="13568-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="13568-127"><dt>**Ungültiges PDH- \_ \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="13568-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="13568-128">Das Handle ist kein gültiges PDH-Objekt.</span><span class="sxs-lookup"><span data-stu-id="13568-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="13568-129"><dt>**Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13568-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="13568-130">Die angegebene Protokolldatei kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="13568-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="13568-131"><dt>**PDH- \_ Datei wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="13568-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="13568-132">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="13568-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="13568-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13568-133">Requirements</span></span>



| <span data-ttu-id="13568-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13568-134">Requirement</span></span> | <span data-ttu-id="13568-135">Wert</span><span class="sxs-lookup"><span data-stu-id="13568-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13568-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13568-136">Minimum supported client</span></span><br/> | <span data-ttu-id="13568-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13568-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13568-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13568-138">Minimum supported server</span></span><br/> | <span data-ttu-id="13568-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13568-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13568-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13568-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="13568-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13568-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="13568-142">DLL</span><span class="sxs-lookup"><span data-stu-id="13568-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13568-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13568-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13568-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13568-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13568-145">**Pdhgetlogfilesize**</span><span class="sxs-lookup"><span data-stu-id="13568-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="13568-146">**Pdhvbopenlog**</span><span class="sxs-lookup"><span data-stu-id="13568-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="13568-147">**Pdhvbupdatelog**</span><span class="sxs-lookup"><span data-stu-id="13568-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

