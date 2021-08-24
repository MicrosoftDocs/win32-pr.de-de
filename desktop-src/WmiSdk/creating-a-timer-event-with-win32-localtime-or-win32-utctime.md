---
description: Sie können das Standardmodell von systeminternen Ereignissen und Ereignisfiltern in Kombination mit den Win32 \_ LocalTime- oder Win32 \_ UTCTime-Klassen verwenden, um eine zeitierte Benachrichtigung zu erhalten.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Erstellen eines Timerereignisses mit Win32_LocalTime oder Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f2dc2c3cbec2b87693920c0ed5ca113f7e6a04c9648f0ef2cc4bca9b4fa90f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612410"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Erstellen eines Timerereignisses mit Win32 \_ LocalTime oder Win32 \_ UTCTime

Sie können das Standardmodell von systeminternen Ereignissen und Ereignisfiltern in Kombination mit den [**Win32 \_ LocalTime-**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ UTCTime-Klassen**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) verwenden, um eine zeitierte Benachrichtigung zu erhalten. Die systeminterne Methode ist eine empfohlene Methode zum Generieren von Zeitereignissen, da sie mit dem Rest des Microsoft-Ereignismodells konsistent ist und komplexe Planungsbedingungen unterstützt.

Die [**Klassen Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) und [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sind Singletonklassen im \\ Cimv2-Stammnamespace, die die Systemuhr darstellen. Bei der Abfrage gibt **Win32 \_ LocalTime** die aktuelle Uhrzeit zum Zeitpunkt des Datenabrufs in einer 24-Stunden-Zeit mit lokalem Verweis zurück. Die **Win32 \_ UTCTime-Klasse** gibt die aktuelle Zeit mit UTC-Verweis zurück.

**So generieren Sie Zeit- oder Wiederholungsereignisse mit Win32 \_ LocalTime oder Win32 \_ UTCTime**

-   Richten Sie einen systeminternen Benachrichtigungsereignisfilter für [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) ein, der eine Benachrichtigung für ein bestimmtes Datum und eine bestimmte Uhrzeit anfordert.

Beispiel: Die Ortszeit unter Sommerzeit ist 16:00 Uhr. und der Standort ist GMT -8, dann gibt [**Win32 \_ LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 16 und [**Win32 \_ UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 23 zurück.

Im folgenden Codebeispiel wird beschrieben, wie Sie einen Ereignisfilter erstellen, der jeden Tag um Mitternacht ein sich wiederholendes Ereignis signalisiert.

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

 

 
