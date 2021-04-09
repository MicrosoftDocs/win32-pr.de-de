---
description: Der Netzwerk Lademodus (Asynchronous Transfer Mode, ATM) basiert auf dem Rechenzentrum, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Quality of Service (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867368"
---
# <a name="quality-of-service-telephony-api"></a>Quality of Service (telefonieapi)

Der Netzwerk Lademodus (Asynchronous Transfer Mode, ATM) basiert auf dem Rechenzentrum, und die Unterstützung für ATM wurde vielen Teilen des Betriebssystems hinzugefügt. TAPI unterstützt auch Schlüssel Attribute der Einrichtung von Anrufen in ATM-Einrichtungen. Die wichtigste davon aus der Anwendungsperspektive ist die Möglichkeit, Quality of Service (QoS)-Parameter für eingehende und ausgehende Aufrufe anzufordern, zu aushandeln, zu aushandeln und Anzeichen dafür zu erhalten.

QoS-Informationen in TAPI werden zwischen Anwendungen und Dienstanbietern in [**Flowspec**](/windows/desktop/api/qos/ns-qos-flowspec) -Strukturen ausgetauscht, die in Windows Sockets 2,0 definiert sind.

Anwendungen fordern QoS für ausgehende Aufrufe an, indem Sie die Sitzungs Informationswerte festlegen, bevor Sie eine Kommunikationssitzung starten. Der Dienstanbieter versucht, die angegebene QoS anzugeben, und schlägt fehl, wenn dies nicht möglich ist. Die Anwendung kann dann Ihre Parameter anpassen und den Rückruf erneut versuchen. Nachdem ein-Rückruf erstellt wurde, kann eine Anwendung eine Änderung im QoS anfordern.

TAPI stellt Ereignis Benachrichtigungen für den Besitzer oder die Überwachung von Anwendungen bereit, wenn eine Änderung der QoS-Ebenen vorliegt.

Die Unterstützung für QoS ist nicht auf ATM-Transporte beschränkt. Jeder Dienstanbieter kann QoS-Funktionen implementieren.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

* * TAPI 2. x: * *[**linesetcallqualityofservice**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwsendingflowspecsize**, **dwsendingflowspecoffset**, **dwreceivingflowspecsize** und **dwreceivingflowspecoffset** Member von [**linecallpara**](/windows/win32/api/tapi/ns-tapi-linecallparams) Metern

* * TAPI 3. x: * *[**itbasiccallcontrol:: setqos**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**itqosevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
