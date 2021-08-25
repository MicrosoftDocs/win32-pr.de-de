---
description: PGM verwendet Socketoptionen, um den Zustand festzulegen, Multicastparameter bereitzustellen und andernfalls die Multicastfunktionen zu implementieren.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: PGM-Socketoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e8df8050146774ac79d45594adcccf53a93d295ce42b9f00834aa0d699e83a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860820"
---
# <a name="pgm-socket-options"></a>PGM-Socketoptionen

PGM verwendet Socketoptionen, um den Zustand festzulegen, Multicastparameter bereitzustellen und andernfalls die Multicastfunktionen zu implementieren. Diese Seite gibt an, wie PGM-Socketoptionen festgelegt werden sollen, listet die für PGM verfügbaren Socketoptionen auf und enthält ggf. Verwendungsbeispiele und zusätzliche Informationen zu verschiedenen Optionen. Grundlegende Definitionen der einzelnen PCM-Socketoptionen finden Sie unter [Socketoptionen.](socket-options.md)

**Windows XP:** Reliable Multicast Programming (PGM) wird nicht unterstützt.

Die folgenden Socketoptionen sind für PGM-Absender verfügbar:

<dl> RM \_ LATEJOIN  
GRÖßE \_ DES \_ RM RATE-FENSTERS \_  
RM \_ SEND \_ WINDOW \_ ADV \_ RATE  
RM \_ SENDER \_ STATISTICS  
RM \_ SENDER \_ WINDOW \_ ADVANCE \_ METHOD  
RM \_ SET \_ MCAST \_ TTL  
RM \_ SET \_ MESSAGE \_ BOUNDARY  
RM \_ SET \_ SEND \_ IF  
RM \_ USE \_ FEC  
</dl>

Die \_ RM SENDER \_ WINDOW ADVANCE \_ \_ METHOD-Option gibt die Methode an, die verwendet wird, wenn das nachfolgende Edge-Sendefenster vorangestellt wird. Der optval-Parameter kann nur E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (Standardeinstellung) sein. Beachten Sie, dass E \_ WINDOW USE AS DATA CACHE nicht unterstützt \_ \_ \_ \_ wird.

Die folgenden Socketoptionen sind für PGM-Empfänger verfügbar:

<dl> RM \_ ADD \_ RECEIVE \_ IF  
RM \_ DEL \_ RECEIVE \_ IF  
RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT  
\_ \_ RM-EMPFÄNGERSTATISTIKEN  
</dl>

## <a name="setting-pgm-socket-options"></a>Festlegen von PGM-Socketoptionen

Der folgende Codeausschnitt veranschaulicht eine Programmierrichtlinie zum Festlegen von PGM-Socketoptionen:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



Im obigen Codeausschnitt hängen Typ und Inhalt von *OptionData* von der festgelegten Socketoption ab. Für alle PGM-Socketoptionen lautet die Socketebene IPPROTO \_ RM. PGM-Socketoptionen müssen unmittelbar nach dem Aufruf der [**bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) mit den folgenden Ausnahmen festgelegt werden:

<dl> RM \_ SET \_ MESSAGE \_ BOUNDARY  
RM \_ SENDER \_ STATISTICS  
\_ \_ RM-EMPFÄNGERSTATISTIKEN  
</dl>

 

 



