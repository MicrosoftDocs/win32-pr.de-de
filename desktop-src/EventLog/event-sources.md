---
description: Jedes Protokoll im EventLog-Schlüssel enthält Unterschlüssel, die als Ereignis Quellen bezeichnet werden. Die Ereignis Quelle ist der Name der Software, von der das Ereignis protokolliert wird.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Ereignisquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345895"
---
# <a name="event-sources"></a><span data-ttu-id="5af1f-104">Ereignisquellen</span><span class="sxs-lookup"><span data-stu-id="5af1f-104">Event Sources</span></span>

<span data-ttu-id="5af1f-105">Jedes Protokoll im [EventLog-Schlüssel](eventlog-key.md) enthält Unterschlüssel, die als *Ereignis Quellen* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="5af1f-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="5af1f-106">Die Ereignis Quelle ist der Name der Software, von der das Ereignis protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="5af1f-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="5af1f-107">Dies ist häufig der Name der Anwendung oder der Name einer Unterkomponente der Anwendung, wenn die Anwendung groß ist.</span><span class="sxs-lookup"><span data-stu-id="5af1f-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="5af1f-108">Sie können der Registrierung maximal 16.384 Ereignis Quellen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="5af1f-109">Das **Sicherheits** Protokoll ist nur für die Verwendung durch das System vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="5af1f-110">Gerätetreiber sollten ihre Namen dem **System** Protokoll hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="5af1f-111">Anwendungen und Dienste sollten ihre Namen dem **Anwendungs** Protokoll hinzufügen oder ein benutzerdefiniertes Protokoll erstellen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="5af1f-112">Die Struktur der Ereignis Quellen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5af1f-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="5af1f-113">Sie können keinen Quellnamen verwenden, der bereits als Protokoll Name verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5af1f-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="5af1f-114">Außerdem können Quellnamen nicht hierarchisch sein. Das heißt, Sie dürfen keinen umgekehrten Schrägstrich (" \\ ") enthalten.</span><span class="sxs-lookup"><span data-stu-id="5af1f-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="5af1f-115">Jede Ereignis Quelle enthält Informationen (z. b. eine [Nachrichtendatei](message-files.md)), die für die Software spezifisch sind, die die Ereignisse protokolliert, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5af1f-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5af1f-116">Registrierungs Wert</span><span class="sxs-lookup"><span data-stu-id="5af1f-116">Registry Value</span></span></th>
<th><span data-ttu-id="5af1f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5af1f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5af1f-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="5af1f-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="5af1f-119">Anzahl der unterstützten Ereignis Kategorien.</span><span class="sxs-lookup"><span data-stu-id="5af1f-119">Number of event categories supported.</span></span> <span data-ttu-id="5af1f-120">Dieser Wert ist vom Typ <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="5af1f-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5af1f-121"><strong>Categorymessagefile</strong></span><span class="sxs-lookup"><span data-stu-id="5af1f-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="5af1f-122">Der Pfad zur kategorienachrichtendatei.</span><span class="sxs-lookup"><span data-stu-id="5af1f-122">Path to the category message file.</span></span> <span data-ttu-id="5af1f-123">Eine kategorienachrichtendatei enthält sprachabhängige Zeichen folgen, die die Kategorien beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5af1f-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="5af1f-124">Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="5af1f-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5af1f-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="5af1f-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="5af1f-126">Der Pfad zu einer oder mehreren Ereignis Meldungs Dateien. Verwenden Sie ein Semikolon, um mehrere Dateien zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="5af1f-127">Eine Ereignis Nachrichtendatei enthält sprachabhängige Zeichen folgen, die die Ereignisse beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5af1f-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="5af1f-128">Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="5af1f-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5af1f-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="5af1f-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="5af1f-130">Der Pfad zur Parameter Nachrichtendatei.</span><span class="sxs-lookup"><span data-stu-id="5af1f-130">Path to the parameter message file.</span></span> <span data-ttu-id="5af1f-131">Eine Parameter Nachrichtendatei enthält sprachunabhängige Zeichen folgen, die in die Ereignis Beschreibungs Zeichenfolgen eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="5af1f-132">Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="5af1f-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5af1f-133"><strong>Typessupported</strong></span><span class="sxs-lookup"><span data-stu-id="5af1f-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="5af1f-134">Bitmaske unterstützter Typen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-134">Bitmask of supported types.</span></span> <span data-ttu-id="5af1f-135">Dieser Wert ist vom Typ <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="5af1f-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="5af1f-136">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="5af1f-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="5af1f-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="5af1f-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="5af1f-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="5af1f-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="5af1f-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="5af1f-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="5af1f-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="5af1f-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="5af1f-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="5af1f-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5af1f-142">Wenn eine Anwendung die [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) -Funktion oder die [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) -Funktion verwendet, um ein Handle für ein Ereignisprotokoll zu erhalten, sucht der Ereignis Protokollierungs Dienst nach der angegebenen Ereignis Quelle in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5af1f-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="5af1f-143">Beispielsweise kann das **Anwendungs** Protokoll Ereignis Quellen für Microsoft SQL Server und Microsoft Excel enthalten.</span><span class="sxs-lookup"><span data-stu-id="5af1f-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="5af1f-144">Wenn eine Anwendung " [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) " oder " **OpenEventLog** " mit dem Quellnamen "Application", "SQL" oder "Excel" verwendet, gibt der Ereignis Protokollierungs Dienst ein Handle an das **Anwendungs** Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="5af1f-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="5af1f-145">Eine Anwendung kann das **Anwendungs** Protokoll verwenden, ohne der Registrierung eine neue Ereignis Quelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5af1f-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="5af1f-146">Wenn die Anwendung [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) aufruft und einen Quellnamen übergibt, der in der Registrierung nicht gefunden werden kann, verwendet der Ereignis Protokollierungs Dienst standardmäßig das **Anwendungs** Protokoll.</span><span class="sxs-lookup"><span data-stu-id="5af1f-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="5af1f-147">Da jedoch keine Nachrichten Dateien vorhanden sind, kann der Ereignisanzeige keine Ereignis Bezeichner oder Ereignis Kategorien einer Beschreibungs Zeichenfolge zuordnen und zeigt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5af1f-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="5af1f-148">Aus diesem Grund sollten Sie der Registrierung eine eindeutige Ereignis Quelle für Ihre Anwendung hinzufügen und eine Nachrichtendatei angeben.</span><span class="sxs-lookup"><span data-stu-id="5af1f-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



