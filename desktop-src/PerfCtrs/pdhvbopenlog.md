---
description: Die pdhvbopenlog-Funktion öffnet die angegebene Protokolldatei zum Lesen und schreiben. Diese Funktion ruft pdhopenlog auf.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: Pdhvbopenlog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529114"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="fc5be-104">Pdhvbopenlog-Funktion</span><span class="sxs-lookup"><span data-stu-id="fc5be-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="fc5be-105">Die **pdhvbopenlog** -Funktion öffnet die angegebene Protokolldatei zum Lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="fc5be-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="fc5be-106">Diese Funktion ruft [**pdhopenlog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)auf.</span><span class="sxs-lookup"><span data-stu-id="fc5be-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc5be-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="fc5be-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="fc5be-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="fc5be-109">Funktion "pdhvbopenlog" ( \_ ByVal szLogFileName als LPCTSTR, \_ ByVal dwaccessflags as DWORD, \_ ByVal lpdwlogtype as LPDWORD, \_ ByVal hquery as PDH \_ hquery, \_ ByVal dwmaxsize as DWORD, \_ ByVal szusercaption as LPCSTR, \_ ByRef phlog as PDH \_ hlog \_ ) As DWORD</span><span class="sxs-lookup"><span data-stu-id="fc5be-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="fc5be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc5be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5be-111">*szLogFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-112">Ein Zeiger auf eine Zeichenfolge, die den Namen der zu öffnenden Protokolldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="fc5be-113">Wenn die Protokolldatei SQL-Daten enthält, lautet das Format des Namens der Protokolldatei " **SQL:**_DataSourceName_*_!"._* _Protokoll Dateiname_.</span><span class="sxs-lookup"><span data-stu-id="fc5be-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="fc5be-114">In diesem Fall lautet der Wert des *lpdwlogtype* -Parameters PDH \_ log \_ Type \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="fc5be-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="fc5be-115">*dwaccessflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-116">Der Zugriffstyp, der beim Öffnen der Protokolldatei angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc5be-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="fc5be-117">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="fc5be-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fc5be-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fc5be-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="fc5be-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fc5be-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="fc5be-120"><dt>**PDH- \_ Protokoll \_ Lese \_ Zugriff**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="fc5be-121">Eine Protokolldatei wird für einen Lesevorgang geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc5be-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="fc5be-122"><dt>**PDH- \_ Protokoll \_ Schreib \_ Zugriff**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="fc5be-123">Eine neue Protokolldatei wird für einen Schreibvorgang geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc5be-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="fc5be-124"><dt>**PDH- \_ Protokoll \_ Aktualisierungs \_ Zugriff**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="fc5be-125">Eine vorhandene Protokolldatei wird für einen Schreibvorgang geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc5be-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="fc5be-126">Der aus der vorherigen Tabelle ausgewählte Wert kann mithilfe des OR-Operators mit einem der folgenden CREATE Access-Flags kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="fc5be-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fc5be-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="fc5be-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fc5be-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="fc5be-129"><dt>**PDH \_ - \_ Protokoll \_ neu erstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="fc5be-130">Eine neue Protokolldatei mit dem angegebenen Namen wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="fc5be-131"><dt>**PDH \_ - \_ Protokoll \_ immer erstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="fc5be-132">Eine neue Protokolldatei mit dem angegebenen Namen wird erstellt, und vorhandene Protokolldateien mit demselben Namen werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fc5be-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="fc5be-133"><dt>**vorhandenes PDH- \_ Protokoll \_ Öffnen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="fc5be-134">Eine vorhandene Protokolldatei mit dem angegebenen Namen wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc5be-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="fc5be-135">Wenn keine Protokolldatei mit dem angegebenen Namen vorhanden ist, entspricht dies dem PDH- \_ Protokoll \_ Create \_ New.</span><span class="sxs-lookup"><span data-stu-id="fc5be-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="fc5be-136"><dt>**PDH \_ - \_ Protokoll \_ immer öffnen**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="fc5be-137">Eine vorhandene Protokolldatei mit dem angegebenen Namen wird geöffnet, oder es wird eine neue Protokolldatei mit dem angegebenen Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="fc5be-138">*lpdwlogtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-139">Ein Zeiger auf eine Variable, die den Typ der zu öffnenden Protokolldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="fc5be-140">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="fc5be-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fc5be-141">Wert</span><span class="sxs-lookup"><span data-stu-id="fc5be-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="fc5be-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fc5be-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="fc5be-143"><dt>**PDH \_ - \_ protokolllistyp nicht \_ definiert**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="fc5be-144">Nicht definiertes Protokolldatei Format.</span><span class="sxs-lookup"><span data-stu-id="fc5be-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="fc5be-145"><dt>**PDH \_ - \_ logstyp \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="fc5be-146">Text Dateien, die Spaltenüberschriften in der ersten Zeile enthalten, und einzelne Daten Beispiele in jeder nachfolgenden Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc5be-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="fc5be-147"><dt>**PDH \_ - \_ Protokolltyp \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="fc5be-148">Die Daten in der Protokolldatei befinden sich in SQL.</span><span class="sxs-lookup"><span data-stu-id="fc5be-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="fc5be-149"><dt>**PDH \_ - \_ protokoltentyp \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="fc5be-150">Identisch mit dem PDH- \_ \_ logstyp \_ CSV.</span><span class="sxs-lookup"><span data-stu-id="fc5be-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="fc5be-151"><dt>**PDH \_ - \_ protokoltentyp \_ Binär**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="fc5be-152">Binäres Protokolldatei Format.</span><span class="sxs-lookup"><span data-stu-id="fc5be-152">Binary log file format.</span></span> <span data-ttu-id="fc5be-153">Schließt Zirkuläre Protokolldateien ein.</span><span class="sxs-lookup"><span data-stu-id="fc5be-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="fc5be-154"><dt>**PDH \_ - \_ protokolllistyp \_ Perfmon**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="fc5be-155">Perfmon-Protokolldatei Format.</span><span class="sxs-lookup"><span data-stu-id="fc5be-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="fc5be-156">*hquery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-157">Abfrage handle.</span><span class="sxs-lookup"><span data-stu-id="fc5be-157">Query handle.</span></span> <span data-ttu-id="fc5be-158">Dieses Handle wird von der [**pdhvbopenquery**](pdhvbopenquery.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc5be-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="fc5be-159">Dieser Parameter kann **null** sein, wenn die Protokolldatei zum Lesen geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc5be-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="fc5be-160">*dwmaxsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-161">Maximale Größe der Protokolldatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc5be-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="fc5be-162">Dieser Wert wird nur verwendet, wenn die Protokolldatei eine begrenzte Größe oder eine zirkuläre Protokolldatei ist.</span><span class="sxs-lookup"><span data-stu-id="fc5be-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="fc5be-163">*szusercaption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-164">Ein Zeiger auf eine Zeichenfolge, die die benutzerdefinierte Beschriftung der Protokolldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="fc5be-165">Im Allgemeinen wird der Inhalt der Protokolldatei durch eine Beschriftung der Protokolldatei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc5be-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="fc5be-166">Wenn eine vorhandene Protokolldatei geöffnet wird, wird der Wert dieses Parameters ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fc5be-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="fc5be-167">*phlog* \[ in, Ref\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5be-168">Ein Zeiger auf einen Puffer, der ein Handle für die geöffnete Protokolldatei empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5be-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc5be-169">Return value</span></span>

<span data-ttu-id="fc5be-170">Wenn die Funktion erfolgreich ausgeführt wird, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc5be-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="fc5be-171">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fc5be-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="fc5be-172">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="fc5be-172">The following are possible values.</span></span>



| <span data-ttu-id="fc5be-173">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fc5be-173">Return code</span></span>                                                                                                | <span data-ttu-id="fc5be-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc5be-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc5be-175"><dt>**nicht genügend PDH- \_ \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="fc5be-176">Die angeforderten Daten sind größer als der angegebene Puffer.</span><span class="sxs-lookup"><span data-stu-id="fc5be-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="fc5be-177">Die angeforderten Daten können nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="fc5be-178"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="fc5be-179">Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.</span><span class="sxs-lookup"><span data-stu-id="fc5be-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="fc5be-180"><dt>**Ungültiges PDH- \_ \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="fc5be-181">Das Handle ist kein gültiges PDH-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc5be-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="fc5be-182"><dt>**Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="fc5be-183">Die angegebene Protokolldatei kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="fc5be-184"><dt>**PDH- \_ Datei wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="fc5be-185">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="fc5be-186">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc5be-186">Remarks</span></span>

<span data-ttu-id="fc5be-187">Wenn Sie diese Funktion verwenden, um Leistungsdaten in eine Protokolldatei zu schreiben, muss zuerst eine Abfrage mit [**pdhvbopenquery**](pdhvbopenquery.md)geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="fc5be-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="fc5be-188">Es muss eine aktuell geöffnete Abfrage vorhanden sein, und die gewünschten Zähler müssen hinzugefügt werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fc5be-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="fc5be-189">Beachten Sie, dass Protokolldateien im Perfmon-Format nur zum Lesen geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fc5be-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5be-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc5be-190">Requirements</span></span>



| <span data-ttu-id="fc5be-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc5be-191">Requirement</span></span> | <span data-ttu-id="fc5be-192">Wert</span><span class="sxs-lookup"><span data-stu-id="fc5be-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5be-193">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc5be-193">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5be-194">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc5be-195">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc5be-195">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5be-196">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc5be-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc5be-197">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fc5be-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc5be-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc5be-199">DLL</span><span class="sxs-lookup"><span data-stu-id="fc5be-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc5be-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc5be-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc5be-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc5be-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5be-202">**Pdhoptolog**</span><span class="sxs-lookup"><span data-stu-id="fc5be-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="fc5be-203">**Pdhvbgetlogfilesize**</span><span class="sxs-lookup"><span data-stu-id="fc5be-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="fc5be-204">**Pdhvbupdatelog**</span><span class="sxs-lookup"><span data-stu-id="fc5be-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

