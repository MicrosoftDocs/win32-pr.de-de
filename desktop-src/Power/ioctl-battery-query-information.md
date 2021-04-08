---
description: Ruft eine Vielzahl von Informationen für den Akku ab.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959743"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="f0d7a-103">Steuerungs Code der IOCTL- \_ Akku \_ Abfrage \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="f0d7a-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="f0d7a-104">Ruft eine Vielzahl von Informationen für den Akku ab.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="f0d7a-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="f0d7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0d7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d7a-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-108">Ein Handle für den Akku, auf dem Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="f0d7a-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-111">The control code for the operation.</span></span> <span data-ttu-id="f0d7a-112">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="f0d7a-113">Verwenden Sie für diesen Vorgang **IOCTL- \_ Akku \_ Abfrage \_ Informationen** .</span><span class="sxs-lookup"><span data-stu-id="f0d7a-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-115">Ein Zeiger auf eine [**Akku \_ Abfrage \_ Informations**](battery-query-information-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-118">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-119">Ein Zeiger auf den Rückgabe Puffer.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-119">A pointer to the return buffer.</span></span> <span data-ttu-id="f0d7a-120">Der Datentyp (und somit die Größe) des Rückgabe Puffers hängt von den Informationen ab, die in der **Akku \_ Abfrage Informations \_ \_ Ebene** der Eingabe- [**Akku- \_ Abfrage \_ Informations**](battery-query-information-str.md) Struktur angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="f0d7a-121">In der folgenden Tabelle werden die von einer bestimmten Informationsebene zurückgegebenen Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="f0d7a-122">Informationsebene</span><span class="sxs-lookup"><span data-stu-id="f0d7a-122">Information level</span></span>                 | <span data-ttu-id="f0d7a-123">Zurückgegebene Daten</span><span class="sxs-lookup"><span data-stu-id="f0d7a-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d7a-124">**Batterydevicename**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="f0d7a-125">Eine mit **null** beendete Unicode-Zeichenfolge, die den Namen des Akkus angibt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f0d7a-126">**Batteryestimatedtime**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="f0d7a-127">Ein **ulong** -Wert, der die geschätzte Akkulaufzeit in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="f0d7a-128">Wenn die für das **atrate** -Element der Struktur der [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md) angegebene Ausgleichs Rate 0 (null) ist, basiert diese Berechnung auf der aktuellen Rate des Ausgleichs.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="f0d7a-129">Wenn **atate** ungleich NULL ist, ist die zurückgegebene Zeit die erwartete Laufzeit für die angegebene Rate.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="f0d7a-130">Wenn die geschätzte Zeit unbekannt ist (z. b. wenn der Akku nicht entladen wird und **atate** NULL ist), wird die **\_ unbekannte Akku \_ Zeit** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="f0d7a-131">Beachten Sie, dass dieser Wert für einige Akku Systeme nicht sehr genau ist.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="f0d7a-132">Der Wert kann abhängig von der aktuellen Stromversorgung, die von der Datenträger Aktivität und anderen Faktoren betroffen sein könnte, stark variieren.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="f0d7a-133">Es gibt keinen Benachrichtigungs Mechanismus für Änderungen dieses Werts.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="f0d7a-134">**Batterygranularityinformation**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="f0d7a-135">Ein Array variabler Länge mit [**Akku \_ Berichterstattungs- \_ Skalierungs**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) Strukturen, das die Granularität der Berichterstellung für die Akkukapazität enthält, die vom [**IOCTL- \_ Akku \_ Abfrage \_ Status**](ioctl-battery-query-status.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="f0d7a-136">Wenn die Granularität von der aktuellen Kapazität des Akkus abhängt, werden mehrere Einträge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="f0d7a-137">Die Interpretation des Arrays von Einträgen finden Sie unter **Akku \_ Bericht \_** Erstellung.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="f0d7a-138">Die Anzahl der Einträge wird durch die Größe des zurückgegebenen Puffers angegeben und kann als (*lpbytesgab* /sizeof (**Akku \_ Berichterstattungs \_ Skala**)) berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="f0d7a-139">Die maximale Anzahl von Einträgen, die zurückgegeben werden, ist vier.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="f0d7a-140">**Akku Informationen**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-140">**BatteryInformation**</span></span>            | <span data-ttu-id="f0d7a-141">Eine [**Akku \_ Informations**](battery-information-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f0d7a-142">**Batterymanufacturedate**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="f0d7a-143">Eine [**Akku \_ Herstellungs \_ Datums**](battery-manufacture-date-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f0d7a-144">**Batterymanufacturename**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="f0d7a-145">Eine auf **null** endenden Unicode-Zeichenfolge, die den Namen des Herstellers des Akkus enthält.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f0d7a-146">**Akku serialNumber**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="f0d7a-147">Eine mit **null** beendete Unicode-Zeichenfolge, die die Seriennummer des Akkus enthält.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f0d7a-148">**Akku Temperatur**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="f0d7a-149">Ein **ulong** -Wert, der die aktuelle Temperatur des Akkus in Zehntel Grad Kelvin enthält.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f0d7a-150">**Batteryuniqueid**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="f0d7a-151">Eine mit **null** beendete Unicode-Zeichenfolge, die den Akku eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="f0d7a-152">Dieser Wert kann verwendet werden, um einen bestimmten Akku zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="f0d7a-153">Im Fall von intelligenten Akkus ist diese ID die Verkettung aus dem Namen des Herstellers, dem Gerätenamen, dem Erstellungsdatum und der druckbaren Darstellung der Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="f0d7a-154">Dieser Wert sollte nicht für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="f0d7a-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-156">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="f0d7a-157">Abhängig von der Informationsebene der angeforderten Daten kann dies ein Puffer mit variabler Größe sein.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-158">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-159">Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer zurückgegebenen Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="f0d7a-160">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, dann schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode **Fehler \_ unzureichend \_** zurück, und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f0d7a-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="f0d7a-161">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="f0d7a-162">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="f0d7a-163">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="f0d7a-164">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7a-165">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="f0d7a-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="f0d7a-166">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f0d7a-167">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="f0d7a-168">In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="f0d7a-169">Wenn das Gerät mit dem überlappenden Flag für das **\_ Dateiflag \_** geöffnet wurde und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="f0d7a-170">Wenn *hdevice* ohne Angabe des überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d7a-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0d7a-171">Return value</span></span>

<span data-ttu-id="f0d7a-172">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="f0d7a-173">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="f0d7a-174">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="f0d7a-175">Einige Informationen zu Akkus sind optional oder für einige Akkus bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="f0d7a-176">Wenn der jeweilige angeforderte Datentyp für den aktuellen Akku nicht verfügbar ist, wird **die \_ Fehler \_ Funktion "ungültig** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="f0d7a-177">Alle Anforderungen für Akku Informationen werden mit dem Status der **Fehler \_ Datei \_ nicht \_ gefunden** , wenn das Element " **batterytag** " der Anforderung nicht mit der des aktuellen Akku Tags identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="f0d7a-178">Dadurch wird sichergestellt, dass die zurückgegebenen Akku Informationen mit denen des angeforderten Akkus übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="f0d7a-179">(Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="f0d7a-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="f0d7a-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0d7a-180">Remarks</span></span>

<span data-ttu-id="f0d7a-181">Diese Akku-ioctl Ruft eine Vielzahl von Informationen für den Akku ab.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="f0d7a-182">Die Eingabeparameter Struktur, die [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md), gibt den Typ der Informationen an, die zurückgegeben werden sollen, und wann die Akku Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="f0d7a-183">Der Datentyp und der Inhalt des Ausgabepuffers variieren basierend auf den angeforderten Daten.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="f0d7a-184">Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".</span><span class="sxs-lookup"><span data-stu-id="f0d7a-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="f0d7a-185">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0d7a-185">Examples</span></span>

<span data-ttu-id="f0d7a-186">Ein Beispiel finden Sie unter Auflisten von [Akku Geräten](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f0d7a-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d7a-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0d7a-187">Requirements</span></span>



| <span data-ttu-id="f0d7a-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0d7a-188">Requirement</span></span> | <span data-ttu-id="f0d7a-189">Wert</span><span class="sxs-lookup"><span data-stu-id="f0d7a-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d7a-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0d7a-190">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d7a-191">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0d7a-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="f0d7a-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0d7a-192">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d7a-193">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0d7a-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="f0d7a-194">Header</span><span class="sxs-lookup"><span data-stu-id="f0d7a-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d7a-195"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="f0d7a-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d7a-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0d7a-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d7a-197">Akku Informationen</span><span class="sxs-lookup"><span data-stu-id="f0d7a-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="f0d7a-198">Steuerungs Codes der Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f0d7a-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="f0d7a-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="f0d7a-200">**Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="f0d7a-201">**\_Skalierung von Akku Berichten \_**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="f0d7a-202">**IOCTL \_ Akku \_ Query- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="f0d7a-203">**IOCTL \_ Akku \_ - \_ abfragetag**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="f0d7a-204">**IOCTL- \_ Akku \_ Satz \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f0d7a-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

