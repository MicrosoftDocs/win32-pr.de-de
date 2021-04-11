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
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime

Sie können das Standardmodell der systeminternen Ereignisse und Ereignis Filter in Kombination mit den Win32-Klassen [**\_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) verwenden, um eine zeitgesteuerte Benachrichtigung zu erhalten. Die intrinsische Methode ist eine empfohlene Methode zum Erstellen von zeitgesteuerten Ereignissen, da Sie mit dem Rest des Microsoft-Ereignis Modells konsistent ist und komplexe Planungsbedingungen unterstützt.

Die [**Win32-Klassen \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) und [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sind Singleton-Klassen im root \\ CIMV2-Namespace, die die Systemuhr darstellen. Beim Abfragen gibt **Win32 \_ localtime** die aktuelle Zeit zum Zeitpunkt des Datenabrufs in einem 24-Stunden-Format mit lokalem Verweis zurück. Die **Win32 \_ utcTime** -Klasse gibt die aktuelle Uhrzeit mit dem UTC-Verweis zurück.

**So generieren Sie zeitgesteuerte oder sich wiederholende Ereignisse mit Win32 \_ localtime oder Win32 \_ utcTime**

-   Richten Sie einen systeminternen Benachrichtigungs Ereignis Filter für [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) ein, der eine Benachrichtigung für ein bestimmtes Datum und eine bestimmte Uhrzeit anfordert.

Wenn z. b. die Ortszeit unter Sommerzeit 4 Uhr ist. und der Speicherort ist GMT-8, dann gibt [**Win32 \_ localtime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) den Wert 16 zurück, und [**Win32 \_ utcTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) gibt 23 zurück.

Im folgenden Codebeispiel wird beschrieben, wie ein Ereignis Filter erstellt wird, der jeden Tag um Mitternacht ein wiederholtes Ereignis signalisiert.

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

 

 
