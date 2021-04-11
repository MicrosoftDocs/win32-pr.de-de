---
description: Sie können das Standardmodell der systeminternen Ereignisse und Ereignis Filter in Kombination mit den Win32- \_ Klassen localtime oder Win32 \_ utcTime verwenden, um eine zeitgesteuerte Benachrichtigung zu erhalten.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Erstellen eines Zeit Geber Ereignisses mit Win32_LocalTime oder Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217963"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="ef05b-103">Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime</span><span class="sxs-lookup"><span data-stu-id="ef05b-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="ef05b-104">Sie können das Standardmodell der systeminternen Ereignisse und Ereignis Filter in Kombination mit den Win32-Klassen [**\_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) verwenden, um eine zeitgesteuerte Benachrichtigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef05b-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="ef05b-105">Die intrinsische Methode ist eine empfohlene Methode zum Erstellen von zeitgesteuerten Ereignissen, da Sie mit dem Rest des Microsoft-Ereignis Modells konsistent ist und komplexe Planungsbedingungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef05b-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="ef05b-106">Die [**Win32-Klassen \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) und [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sind Singleton-Klassen im root \\ CIMV2-Namespace, die die Systemuhr darstellen.</span><span class="sxs-lookup"><span data-stu-id="ef05b-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="ef05b-107">Beim Abfragen gibt **Win32 \_ localtime** die aktuelle Zeit zum Zeitpunkt des Datenabrufs in einem 24-Stunden-Format mit lokalem Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="ef05b-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="ef05b-108">Die **Win32 \_ utcTime** -Klasse gibt die aktuelle Uhrzeit mit dem UTC-Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="ef05b-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="ef05b-109">**So generieren Sie zeitgesteuerte oder sich wiederholende Ereignisse mit Win32 \_ localtime oder Win32 \_ utcTime**</span><span class="sxs-lookup"><span data-stu-id="ef05b-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="ef05b-110">Richten Sie einen systeminternen Benachrichtigungs Ereignis Filter für [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) ein, der eine Benachrichtigung für ein bestimmtes Datum und eine bestimmte Uhrzeit anfordert.</span><span class="sxs-lookup"><span data-stu-id="ef05b-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="ef05b-111">Wenn z. b. die Ortszeit unter Sommerzeit 4 Uhr ist.</span><span class="sxs-lookup"><span data-stu-id="ef05b-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="ef05b-112">und der Speicherort ist GMT-8, dann gibt [**Win32 \_ localtime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) den Wert 16 zurück, und [**Win32 \_ utcTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) gibt 23 zurück.</span><span class="sxs-lookup"><span data-stu-id="ef05b-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="ef05b-113">Im folgenden Codebeispiel wird beschrieben, wie ein Ereignis Filter erstellt wird, der jeden Tag um Mitternacht ein wiederholtes Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="ef05b-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
