---
description: PGM verwendet Socketoptionen, um den Status festzulegen, Multicast Parameter bereitzustellen und anderweitig seine Multicast Funktionen zu implementieren.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: PGM-Socketoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862544"
---
# <a name="pgm-socket-options"></a>PGM-Socketoptionen

PGM verwendet Socketoptionen, um den Status festzulegen, Multicast Parameter bereitzustellen und anderweitig seine Multicast Funktionen zu implementieren. Diese Seite gibt an, wie PGM-Socketoptionen festgelegt werden sollen, listet die für PGM verfügbaren Socketoptionen auf und stellt Verwendungs Beispiele sowie zusätzliche Informationen für verschiedene Optionen bereit. Grundlegende Definitionen der einzelnen PCM-Socketoptionen finden Sie unter [Socketoptionen](socket-options.md).

**Windows XP:** Die zuverlässige Multicast Programmierung (PGM) wird nicht unterstützt.

Die folgenden Socketoptionen sind für PGM-Absender verfügbar:

<dl> RM- \_ latejoin  
\_ \_ Fenster \_ Größe für RM-Rate  
\_ \_ \_ ADV- \_ Rate der RM-Sendefenster  
RM- \_ Absender \_ Statistik  
vorab Methode des RM- \_ Absender \_ Fensters \_ \_  
RM \_ - \_ mcast- \_ TTL festlegen  
RM \_ Festlegen der \_ Nachrichten \_ Grenze  
RM \_ Set \_ Send \_ if  
RM- \_ Verwendung von \_ FEC  
</dl>

Die Option für die erweiterte Methode des RM- \_ Sender \_ Fensters \_ gibt die Methode an, die \_ verwendet wird, wenn das nachfolgende Edge-Fenster Der optval-Parameter kann nur E \_ Fenster \_ vor \_ \_ der Zeit (Standard) sein. Beachten Sie, dass die E- \_ Window- \_ Verwendung \_ als \_ Daten \_ Cache nicht unterstützt wird.

Die folgenden Socketoptionen sind für PGM-Empfänger verfügbar:

<dl> RM \_ Add \_ Receive \_ if  
RM-ENTF \_ \_ empfangen, \_ Wenn  
RM-Aktivierung mit \_ hoher \_ Geschwindigkeit im \_ Intranet \_  
RM- \_ Empfänger \_ Statistik  
</dl>

## <a name="setting-pgm-socket-options"></a>Festlegen der PGM-Socketoptionen

Der folgende Code Ausschnitt veranschaulicht eine Programmier Richtlinie zum Festlegen der PGM-Socketoptionen:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



Im obigen Code Ausschnitt sind der Typ und der Inhalt von *optiondata* abhängig von der festgelegten Socketoption. Bei allen PGM-Socketoptionen lautet die Socketebene ipproto \_ RM. PGM-Socketoptionen müssen direkt nach dem Aufrufe der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion festgelegt werden, mit den folgenden Ausnahmen:

<dl> RM \_ Festlegen der \_ Nachrichten \_ Grenze  
RM- \_ Absender \_ Statistik  
RM- \_ Empfänger \_ Statistik  
</dl>

 

 



