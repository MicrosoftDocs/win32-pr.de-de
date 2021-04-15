---
title: Netzwerk Ablauf Verfolgung in Windows 7
description: Windows 7 baut auf dem Netzwerk Diagnose Framework (ndf) auf, um eine schnelle Methode zur Behebung von Problemen mit der Netzwerk Konnektivität bereitzustellen, indem die Erfassung aller benötigten Informationen in einem Schritt und die Verwendung der Ereignis Ablauf Verfolgung für Windows (ETW) zum Protokollieren von Netzwerk Ereignis Paketen in einer einzelnen Datei genutzt wird.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390985"
---
# <a name="network-tracing-in-windows-7"></a>Netzwerk Ablauf Verfolgung in Windows 7

Wenn die Komplexität des Netzwerk Stapels zunimmt, ist es oft schwierig, Probleme im Stapel schnell zu verfolgen und zu diagnostizieren. Windows 7 baut auf dem Netzwerk Diagnose Framework (ndf) auf, um eine schnelle Methode zur Behebung von Problemen mit der Netzwerk Konnektivität bereitzustellen, indem die Erfassung aller benötigten Informationen in einem Schritt und die Verwendung der [Ereignis Ablauf Verfolgung für Windows (ETW)](../etw/event-tracing-portal.md) zum Protokollieren von Netzwerk Ereignissen & Paketen in einer einzigen Datei genutzt wird.

Verwandte Ereignisse und Pakete werden für eine bestimmte Aktivität, z. b. das Durchsuchen einer Website, in den verschiedenen Komponenten im Netzwerk Stapel gruppiert. Die Ausgabe dieses Prozesses ist eine ETL-Datei (Event Trace Log, Ereignis Ablauf Verfolgungs Protokoll). Durch das zulassen, dass alle Ereignisse im Zusammenhang mit einer bestimmten Aktivität gleichzeitig in dieser Datei angezeigt werden, kann die Zeit, die zum isolieren und Diagnostizieren von Netzwerkproblemen erforderlich ist, erheblich reduziert werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [Netzwerk Ablauf Verfolgung in Windows 7: Architektur](network-tracing-in-windows-7-architecture.md)                                |
| [Tools zur Problembehandlung mithilfe der Netzwerk Ablauf Verfolgung in Windows 7](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [Netzwerk Ablauf Verfolgung in Windows 7: Szenarios](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 