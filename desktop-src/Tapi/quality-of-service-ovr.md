---
description: Das Netzwerk des asynchronen Übertragungsmodus (ASYNCHRONOUS Transfer Mode, ATM) entwickelt sich zum Mainstream des Computings, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Quality of Service (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761231"
---
# <a name="quality-of-service-telephony-api"></a>Quality of Service (Telefonie-API)

Das Netzwerk des asynchronen Übertragungsmodus (ASYNCHRONOUS Transfer Mode, ATM) entwickelt sich zum Mainstream des Computings, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt. TAPI unterstützt auch wichtige Attribute für das Einrichten von Aufrufen in ATM-Einrichtungen. Das Wichtigste aus Sicht der Anwendung ist die Möglichkeit, Hinweise auf Quality of Service-Parameter (QOS) für eingehende und ausgehende Aufrufe an- und auszuhandeln, neu auszuhandeln und zu empfangen.

QOS-Informationen in TAPI werden zwischen Anwendungen und Dienstanbietern in [**FLOWSPEC-Strukturen**](/windows/desktop/api/qos/ns-qos-flowspec) ausgetauscht, die in Windows Sockets 2.0 definiert sind.

Anwendungen fordern QOS bei ausgehenden Aufrufen an, indem sie Sitzungsinformationswerte festlegen, bevor eine Kommunikationssitzung gestartet wird. Der Dienstanbieter versucht, den angegebenen QOS-Wert anzugeben, und der Aufruf wird nicht unterstützt, wenn dies nicht möglich ist. Die Anwendung kann dann ihre Parameter anpassen und den Aufruf erneut versuchen. Nachdem ein Aufruf eingerichtet wurde, kann eine Anwendung eine Änderung im QOS anfordern.

TAPI stellt Ereignisbenachrichtigungen für Besitzer- oder Monitoranwendungen zur Verfügung, wenn sich die QOS-Ebenen ändern.

Die Unterstützung für QOS ist nicht auf ATM-Transporte beschränkt. Jeder Dienstanbieter kann QOS-Features implementieren.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x: **[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize** und **dwReceivingFlowspecOffset-Member** von [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

**TAPI 3.x: **[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
