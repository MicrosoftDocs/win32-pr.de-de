---
title: Verwenden der PerfLib-Funktionen zum Verarbeiten von Leistungsindikatordaten
description: Perflib-API-Funktionen können verwendet werden, um v2-Leistungs Leistungsdaten direkt zu nutzen, wenn PDH nicht verwendet werden kann.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "106337472"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Verwenden der PerfLib-Funktionen zum Verarbeiten von Leistungsindikatordaten

Verwenden Sie die Perflib-Consumer-Funktionen, um Leistungsdaten von V2-Leistungsdaten Anbietern zu nutzen, wenn Sie keine [PDH-Funktionen (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md)verwenden können. Diese Funktionen können verwendet werden, wenn Sie onecore-Anwendungen schreiben, um v2-Gegensätze zu erfassen, oder wenn Sie v2-Gegensätze mit minimalen Abhängigkeiten und mehr Aufwand erfassen müssen.

> [!TIP]
> Die Perflib v2-consumerfunktionen sind schwieriger zu verwenden als die PDH-Funktionen (Performance Data Helper) und unterstützen nur das Sammeln von Daten von V2-Anbietern. Die PDH-Funktionen sollten für die meisten Anwendungen bevorzugt werden.

Die Perflib v2-consumerfunktionen sind die Low-Level-API zum Erfassen von Daten von **v2-Anbietern**. Die Perflib v2-consumerfunktionen unterstützen das Sammeln von Daten von **v1-Anbietern** nicht.

> [!WARNING]
> Die Perflib v2-consumerfunktionen können möglicherweise Daten aus nicht vertrauenswürdigen Quellen erfassen, z. b. von lokalen Diensten mit eingeschränkten Berechtigungen oder von Remote Computern. Die Perflib v2-consumerfunktionen überprüfen die Daten nicht auf Integrität oder Konsistenz. Es liegt in ihrer Consumeranwendung, zu überprüfen, ob die zurückgegebenen Daten konsistent sind, z. b., dass die Größen Werte im zurückgegebenen Datenblock nicht die tatsächliche Größe des zurückgegebenen Datenblocks überschreiten. Dies ist besonders wichtig, wenn die Consumeranwendung mit erhöhten Rechten ausgeführt wird.

## <a name="perflib-usage"></a>Perflib-Verwendung

Der `perflib.h` -Header enthält die Deklarationen, die von V2-benutzermodusanbietern (d. h. der Perflib-Anbieter-API) und v2-Consumern (d.h. die Perflib-Consumer-API Sie deklariert die folgenden Funktionen für die Nutzung von V2-Leistungsdaten:

- Verwenden Sie [**perfenumeratecounterset**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) , um die GUIDs der Gegensätze abzurufen, die von den V2-Anbietern im System registriert werden.
- Verwenden Sie [**perfquerycountersetregistrationinfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) , um Informationen zu einem bestimmten CounterSet, wie z. b. den Namen, die Beschreibung, den Typ (Einzel Instanz oder mehrere Instanzen), Indikator Typen, Indikator Namen und Indikator Beschreibungen, zu erhalten.
- Verwenden Sie [**perfenumeratecountersetinhaltungen**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) , um die Namen der derzeit aktiven Instanzen eines Gegensatzes mit mehreren Instanzen zu erhalten.
- Verwenden Sie [**perfopenqueryhandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) , um ein neues Abfrage Handle zu erstellen, das zum Sammeln von Daten aus einem oder mehreren Gegensätzen verwendet werden soll.
- Verwenden Sie [**perfclosequeryhandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) , um ein Abfrage Handle zu schließen.
- Verwenden Sie [**perfaddcounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) , um einem Abfrage handle eine Abfrage hinzuzufügen.
- Verwenden Sie [**perfdeletecounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) , um eine Abfrage aus einem Abfrage Handle zu entfernen.
- Verwenden Sie [**perfquerycounterinfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) , um Informationen zu den aktuellen Abfragen für ein Abfrage Handle zu erhalten.
- Verwenden Sie [**perfquerycounterdata**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) , um die Leistungsdaten von einem Abfrage Handle zu erfassen.

Wenn der Consumer nur Daten von einem bestimmten Anbieter beansprucht, bei dem die GUID und die Indikator Indizes stabil sind und Sie Zugriff auf die [ctrpp](ctrpp.md)-generierte Symbol Datei haben (aus dem ctrpp- `-ch` Parameter), können Sie die CounterSet-GUID und die Indikator Indexwerte in den Consumer Hardcodieren.

Andernfalls müssen Sie CounterSet-Metadaten laden, um die in der Abfrage zu verwendenden CounterSet-GUID (s) und Indikator Indizes wie folgt zu ermitteln:

- Verwenden Sie **perfenumeratecounterset** , um eine Liste der unterstützten CounterSet-GUIDs abzurufen.
- Verwenden Sie für jede GUID **perfquerycountersetregistrationinfo** , um den Namen des Gegensatzes zu laden. Beenden Sie den Namen, den Sie suchen.
- Verwenden Sie **perfquerycountersetregistrationinfo** , um die verbleibenden Metadaten (countersetkonfiguration, Indikator Namen, Indikator Indizes, Indikator Typen) für diese gegen Menge zu laden.

Wenn Sie nur die Namen der derzeit aktiven Instanzen eines countersets kennen müssen (d. h., wenn Sie die tatsächlichen Werte für die Leistungsdaten nicht benötigen), können Sie **perfenumeratecountersetinstistiken** verwenden. Dies nimmt eine CounterSet-GUID als Eingabe an und gibt einen- `PERF_INSTANCE_HEADER` Block mit den Namen und IDs der derzeit aktiven Instanzen der angegebenen CounterSet-Instanz zurück.

### <a name="queries"></a>Abfragen

Um Leistungsdaten zu erfassen, müssen Sie ein Abfrage Handle erstellen, ihm Abfragen hinzufügen und die Daten aus den Abfragen sammeln.

Einem Abfrage Handle können viele Abfragen zugeordnet sein. Wenn Sie **perfquerycounterdata** für ein Abfrage handle aufzurufen, führt Perflib alle Abfragen des Handles aus und sammelt alle Ergebnisse.

Jede Abfrage gibt eine CounterSet-GUID, einen instanznamensfilter, einen optionalen Filter für die Instanz-ID und einen optionalen Indikator-ID-Filter an.

- Die CounterSet-GUID ist erforderlich. Gibt die GUID des countersets an, aus dem die Abfrage Daten sammelt. Dies ähnelt der- `FROM` Klausel einer SQL-Abfrage.
- Der instanznamensfilter ist erforderlich. Es gibt ein Platzhalter Muster an, das der Instanzname für die Instanz entsprechen muss, die in die Abfrage eingeschlossen werden soll, wobei `*` "beliebige Zeichen" und `?` "ein Zeichen" angegeben werden. Für einzelinstanzcountersets **muss** dieser auf eine Zeichenfolge der Länge 0 (null) festgelegt werden `""` . Bei Gegensätzen mit mehreren Instanzen **muss** dies auf eine nicht leere Zeichenfolge festgelegt werden (verwenden `"*"` Sie, um alle Instanznamen zu akzeptieren). Dies ist vergleichbar mit einer- `WHERE InstanceName LIKE NameFilter` Klausel einer SQL-Abfrage.
- Der instanzid-Filter ist optional. Wenn vorhanden (d. h., wenn ein anderer Wert als festgelegt `0xFFFFFFFF` ist), gibt dies an, dass die Abfrage nur Instanzen erfassen soll, bei denen die Instanz-ID mit der angegebenen ID übereinstimmt. Wenn kein Wert vorhanden ist (d. h., wenn er auf festgelegt `0xFFFFFFFF` ist), bedeutet dies, dass die Abfrage alle Instanz-IDs Dies ist vergleichbar mit einer- `WHERE InstanceId == IdFilter` Klausel einer SQL-Abfrage.
- Der Filter für die Counter-ID ist optional. Wenn das Element vorhanden ist (d. h., wenn es auf einen anderen Wert als festgelegt ist `PERF_WILDCARD_COUNTER` ), gibt es an, dass die Abfrage einen einzelnen Leistungs Besatz erfassen soll, ähnlich einer `SELECT CounterName` Klausel einer SQL-Abfrage Wenn Sie nicht vorhanden ist (d. h., wenn Sie auf festgelegt `PERF_WILDCARD_COUNTER` ist), gibt Sie an, dass die Abfrage alle verfügbaren Leistungsindikatoren erfassen soll, ähnlich wie bei einer- `SELECT *` Klausel

Verwenden Sie **perfaddcounters** , um Abfragen zu einem Abfrage handle hinzuzufügen. Verwenden Sie **perfdeletecounters** , um Abfragen aus einem Abfrage Handle zu entfernen.

Nachdem Sie die Abfragen in einem Abfrage handle geändert haben, verwenden Sie **perfquerycounterinfo** , um die Abfrage Indizes abzurufen. Die Indizes geben die Reihenfolge an, in der die Abfrageergebnisse von **perfquerycounterdata** zurückgegeben werden (die Ergebnisse entsprechen nicht immer der Reihenfolge, in der die Abfragen hinzugefügt wurden).

Sobald das Abfrage handle fertig ist, können Sie die Daten mit **perfquerycounterdata** erfassen. Normalerweise werden die Daten in regelmäßigen Abständen (einmal pro Sekunde oder einmal pro Minute) gesammelt. Anschließend werden die Daten bei Bedarf verarbeitet.

> [!NOTE]
> Leistungsindikatoren sind nicht so konzipiert, dass Sie mehr als einmal pro Sekunde erfasst werden.

**Perfquerycounterdata** gibt einen- `PERF_DATA_HEADER` Block zurück, der aus einem Daten Header mit Zeitstempeln besteht, gefolgt von einer Sequenz von- `PERF_COUNTER_HEADER` Blöcken, die jeweils die Ergebnisse einer Abfrage enthalten.

Der `PERF_COUNTER_HEADER` kann verschiedene Arten von Daten enthalten, die durch den Wert des-Felds angegeben werden `dwType` :

- `PERF_ERROR_RETURN` -PERFLIB kann keine gültigen Leistungsdaten des Anbieters zurückerhalten.
- `PERF_SINGLE_COUNTER` -Die Abfrage war für einen einzelnen Indikator aus einer einzelinstanzcountermenge. Die Ergebnisse enthalten nur den angeforderten Leistungs Zählers.
- `PERF_MULTIPLE_COUNTERS` -Die Abfrage war für mehrere Leistungsindikatoren aus einer einzelinstanzcountermenge. Das Ergebnis enthält die Werte für die Leistungswerte sowie Informationen zum Abgleich der einzelnen Werte mit dem entsprechenden Leistungs BEWERT (d. h. Spaltenüberschriften).
- `PERF_MULTIPLE_INSTANCES` -Die Abfrage war für einen einzelnen Indikator aus einer gegen Gruppe mit mehreren Instanzen vorgesehen. Die Ergebnisse enthalten die Instanzinformationen (d. h. Zeilen Überschriften) und einen Leistungswert pro Instanz.
- `PERF_COUNTERSET` -Die Abfrage war für mehrere Leistungsindikatoren von einem gegen Satz mit mehreren Instanzen. Die Ergebnisse enthalten die Instanzinformationen (d. h. Zeilen Überschriften), die Leistungswerte der einzelnen Instanzen sowie Informationen zum Abgleich der einzelnen Werte mit dem entsprechenden Leistungs Bezeichner (d. h. Spaltenüberschriften).

Die von **perfquerycounterdata** zurückgegebenen Werte sind `UINT32` oder `UINT64` Rohwerte. Diese erfordern in der Regel einige Verarbeitungsvorgänge, um die erwarteten formatierten Werte zu erhalten. Die erforderliche Verarbeitung hängt vom Typ des Zählers ab. Viele Leistungstypen erfordern zusätzliche Informationen für die gesamte Verarbeitung, wie z. b. einen Zeitstempel oder einen Wert aus einem "Base"-Leistungs bemesser im gleichen Beispiel.

Einige Indikator Typen sind "Delta"-Indikatoren, die im Vergleich mit den Daten aus einem vorherigen Beispiel nur aussagekräftig sind. Beispielsweise weist ein Zähler des Typs `PERF_SAMPLE_COUNTER` einen formatierten Wert auf, bei dem erwartet wird, dass eine Rate angezeigt wird (wie oft ein bestimmter Vorgang pro Sekunde über das Stichproben Intervall eingetreten ist), aber der tatsächliche Rohwert ist nur eine Anzahl (die Häufigkeit, mit der ein bestimmtes Ergebnis aufgetreten ist). Um den formatierten Wert "Rate" zu erhalten, müssen Sie die Formel anwenden, die dem zähtertyp entspricht. Die Formel für `PERF_SAMPLE_COUNTER` ist `(N1 - N0) / ((T1 - T0) / F)` : subtrahieren Sie den Wert des aktuellen Beispiels aus dem Wert des vorherigen Beispiels (gibt an, wie oft das Ereignis während des Samplingintervalls aufgetreten ist), und teilen Sie das Ergebnis dann durch die Anzahl der Sekunden im Abtast Intervall (durch Subtrahieren des Zeitstempels des aktuellen Stichproben aus dem Zeitstempel des vorherigen Beispiels).

Weitere Informationen zum Berechnen von formatierten Werten aus unformatierten Werten finden Sie unter [berechnen](calculating-counter-values.md) von Leistungswerten.

## <a name="sample"></a>Beispiel

Der folgende Code implementiert einen Consumer, der die Perflib v2-consumerfunktionen verwendet, um die CPU-Leistungsinformationen aus dem CounterSet "Prozessor Informationen" zu lesen.

Der Consumer ist wie folgt organisiert:

- Die- `CpuPerfCounters` Klasse implementiert die Logik zum Verarbeiten von Leistungsdaten. Er kapselt ein Abfrage Handle und einen Datenpuffer, in den Abfrageergebnisse aufgezeichnet werden.
- Die- `CpuPerfTimestamp` Struktur speichert die Zeitstempel-Informationen für ein Beispiel. Jedes Mal, wenn Daten gesammelt werden, empfängt der Aufrufer eine einzelne `CpuPerfTimestamp` .
- Die `CpuPerfData` Struktur speichert die Leistungsinformationen (Instanzname und rohleistungs Werte) für eine CPU. Jedes Mal, wenn Daten gesammelt werden, empfängt der Aufrufer ein Array von `CpuPerfData` (einem pro CPU).

In diesem Beispiel werden hart codierte CounterSet-GUID-und Indikator-ID-Werte verwendet, da Sie für eine bestimmte gegen Menge (Prozessor Informationen) optimiert ist, die GUID-oder ID-Werte nicht ändert. Eine allgemeinere Klasse, die Leistungsdaten aus willkürlichen Gegensätzen liest, muss **perfquerycountersetregistrationinfo** verwenden, um die Zuordnung zwischen Indikator-IDs und Indikator Werten zur Laufzeit zu überprüfen.

Ein einfaches `CpuPerfCountersConsumer.cpp` Programm zeigt, wie die Werte aus der- `CpuPerfCounters` Klasse verwendet werden.

### <a name="cpuperfcountersh"></a>Cpuperfcounters. h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>Cpuperfcounters. cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>Cpuperfcountersconsumer. cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
