---
description: Die nteventlogeventconsumer-Klasse protokolliert eine bestimmte Nachricht im Ereignisprotokoll des Betriebssystems, wenn ihr ein Ereignis zugestellt wird.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Nteventlogeventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863323"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="4f516-103">Nteventlogeventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="4f516-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="4f516-104">Die **nteventlogeventconsumer** -Klasse protokolliert eine bestimmte Nachricht im Ereignisprotokoll des Betriebssystems, wenn ihr ein Ereignis zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f516-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="4f516-105">Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f516-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="4f516-106">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="4f516-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f516-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f516-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="4f516-108">Member</span><span class="sxs-lookup"><span data-stu-id="4f516-108">Members</span></span>

<span data-ttu-id="4f516-109">Die **nteventlogeventconsumer** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4f516-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="4f516-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f516-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f516-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f516-111">Properties</span></span>

<span data-ttu-id="4f516-112">Die **nteventlogeventconsumer** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4f516-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f516-113">**Kategorie**</span><span class="sxs-lookup"><span data-stu-id="4f516-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f516-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-116">Ereignis Kategorie.</span><span class="sxs-lookup"><span data-stu-id="4f516-116">Event category.</span></span> <span data-ttu-id="4f516-117">Dies sind Quell spezifische Informationen, die einen beliebigen Wert aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="4f516-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-118">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="4f516-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-119">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="4f516-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4f516-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-121">Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4f516-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="4f516-122">WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="4f516-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="4f516-123">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="4f516-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="4f516-124">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f516-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f516-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="4f516-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f516-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-128">Ereignismeldung in der Nachrichten-dll.</span><span class="sxs-lookup"><span data-stu-id="4f516-128">Event message in the message DLL.</span></span> <span data-ttu-id="4f516-129">Diese Eigenschaft darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4f516-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="4f516-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f516-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-133">Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="4f516-133">Type of event.</span></span> <span data-ttu-id="4f516-134">Dieser Parameter kann einen der in der folgenden Liste aufgeführten Werte aufweisen, die in "Winnt. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4f516-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="4f516-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Ereignisprotokoll \_ Erfolg** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4f516-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-136">Erfolgreiches Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f516-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="4f516-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Ereignisprotokoll \_ Fehler- \_ Tpye** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="4f516-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-138">Fehler Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f516-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="4f516-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Ereignisprotokoll \_ \_Warnungstyp** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="4f516-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-140">Warnungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f516-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="4f516-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Ereignisprotokoll \_ \_Informationstyp** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="4f516-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-142">Informations Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f516-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="4f516-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Ereignisprotokoll \_ Überwachen \_ erfolgreich** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="4f516-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-144">Erfolgreicher Überwachungstyp</span><span class="sxs-lookup"><span data-stu-id="4f516-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="4f516-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Ereignisprotokoll \_ Überwachungs \_ Fehler** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="4f516-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="4f516-146">Fehler Überwachungstyp</span><span class="sxs-lookup"><span data-stu-id="4f516-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4f516-147">**Insertionstringtemplates**</span><span class="sxs-lookup"><span data-stu-id="4f516-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-148">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4f516-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f516-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-150">Array von standardmäßigen Zeichen folgen Vorlagen, die als Einfügezeichenfolge für einen Ereignisprotokoll Daten Satz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f516-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="4f516-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-154">Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="4f516-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="4f516-155">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f516-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f516-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="4f516-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f516-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-159">Maximale Warteschlange für einen bestimmten Consumer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4f516-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="4f516-160">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f516-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f516-161">**Name**</span><span class="sxs-lookup"><span data-stu-id="4f516-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f516-164">Qualifizierer: [ **Schlüssel**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4f516-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="4f516-165">Der eindeutige Name eines Consumers.</span><span class="sxs-lookup"><span data-stu-id="4f516-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-166">**Nameofrawdataproperty**</span><span class="sxs-lookup"><span data-stu-id="4f516-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-169">Der Name der Ereignis Eigenschaft, die Daten enthält, die an die Report [**Event**](/windows/desktop/api/winbase/nf-winbase-reporteventa) -Funktion des *lprawdata* -Parameters übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f516-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-170">**NameOfUserSIDProperty**</span><span class="sxs-lookup"><span data-stu-id="4f516-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-173">Der Name der Ereignis Eigenschaft, die eine Sicherheits-ID (SID) enthält, die an den "Report [**Event**](/windows/desktop/api/winbase/nf-winbase-reporteventa) "-Funktion- *lpusersid* -Parameter übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f516-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="4f516-174">Die-Eigenschaft muss entweder ein Bytearray (**Uint8**) oder eine Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="4f516-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="4f516-175">Wenn es sich um ein Bytearray handelt, wird davon ausgegangen, dass es sich um eine SID handelt.</span><span class="sxs-lookup"><span data-stu-id="4f516-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="4f516-176">Wenn es sich um eine Zeichenfolge handelt, ist es eine Zeichen folgen-sid, die in eine SID konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4f516-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-177">**"Numofinsertionstrings"**</span><span class="sxs-lookup"><span data-stu-id="4f516-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-178">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f516-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-180">Anzahl der Elemente im **insertionstringtemplates** -Array.</span><span class="sxs-lookup"><span data-stu-id="4f516-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="4f516-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="4f516-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-184">Der Name der Quelle, in der sich eine Nachricht befindet.</span><span class="sxs-lookup"><span data-stu-id="4f516-184">Source name where a message is located.</span></span> <span data-ttu-id="4f516-185">Es wird davon ausgegangen, dass der Kunde eine DLL mit den erforderlichen Nachrichten registriert hat.</span><span class="sxs-lookup"><span data-stu-id="4f516-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="4f516-186">Der Wert dieses Parameters darf keinen Doppelpunkt enthalten (:) Art.</span><span class="sxs-lookup"><span data-stu-id="4f516-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f516-187">**Uncservername**</span><span class="sxs-lookup"><span data-stu-id="4f516-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f516-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f516-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f516-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f516-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f516-190">Der Name des Computers, auf dem ein Ereignis protokolliert werden soll, oder **null** , wenn das Ereignis auf einem lokalen Server protokolliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f516-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="4f516-191">Authentifizierte Benutzer können Ereignisse standardmäßig nicht im Anwendungsprotokoll auf einem Remote Computer protokollieren.</span><span class="sxs-lookup"><span data-stu-id="4f516-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="4f516-192">Daher funktioniert die Verwendung dieser Eigenschaft zum Angeben eines Remote Computers nicht.</span><span class="sxs-lookup"><span data-stu-id="4f516-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="4f516-193">Weitere Informationen zum Ändern der Ereignisprotokoll Sicherheit finden Sie in diesem [KB-Artikel](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="4f516-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f516-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f516-194">Remarks</span></span>

<span data-ttu-id="4f516-195">Die **nteventlogeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4f516-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="4f516-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f516-196">Examples</span></span>

<span data-ttu-id="4f516-197">Ein Beispiel für die Verwendung von **nteventlogeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Protokollieren in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="4f516-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f516-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f516-198">Requirements</span></span>



| <span data-ttu-id="4f516-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f516-199">Requirement</span></span> | <span data-ttu-id="4f516-200">Wert</span><span class="sxs-lookup"><span data-stu-id="4f516-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f516-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f516-201">Minimum supported client</span></span><br/> | <span data-ttu-id="4f516-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f516-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f516-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f516-203">Minimum supported server</span></span><br/> | <span data-ttu-id="4f516-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f516-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f516-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f516-205">Namespace</span></span><br/>                | <span data-ttu-id="4f516-206">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="4f516-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="4f516-207">MOF</span><span class="sxs-lookup"><span data-stu-id="4f516-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f516-208"><dt>Wbemcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4f516-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f516-209">DLL</span><span class="sxs-lookup"><span data-stu-id="4f516-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f516-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f516-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f516-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f516-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f516-212">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="4f516-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="4f516-213">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="4f516-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="4f516-214">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="4f516-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="4f516-215">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="4f516-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

