---
description: Unterstützen von MTP-Erweiterungen
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Unterstützen von MTP-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6a5a585167984ec944528bb74a6746e42ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867524"
---
# <a name="supporting-mtp-extensions"></a>Unterstützen von MTP-Erweiterungen

## <a name="media-transfer-protocol"></a>Medien Übertragungsprotokoll

Das Media Transfer Protocol (MTP) ist eine Erweiterung des Picture Transfer-Protokolls (PTP). Folglich sind alle PTP-Protokoll Semantik in MTP gültig.

MTP kommuniziert mithilfe von Befehlen und Antworten zwischen zwei Parteien, dem Initiator und dem Beantworter. Die Rollen der beteiligten Geräte sind eindeutig definiert. Der PC ist in der Regel der Initiator, und das Gerät ist immer der Responder. Ein nicht-PC-Gerät könnte auch ein Initiator (z. b. ein Fahrzeug Stapel oder ein Microsoft X-Box-Gerät) sein. Ein Gerät kann niemals beide Rollen gleichzeitig annehmen.

Der Initiator startet die Kommunikation, indem er einen Befehl an den Beantworter sendet. Der-Beantworter verarbeitet den Befehl und sendet eine entsprechende Antwort zurück. Dem Befehl kann eine Daten Phase zugeordnet sein. Wenn dies der Fall ist, muss die Richtung des Datenflusses im Voraus bekannt sein und vom Initiator und dem Beantworter akzeptiert werden. Beachten Sie, dass es keinen beschreibenden Header gibt, der Datenflüsse für neue Befehle angibt.

Der Beantworter kann die Kommunikation unabhängig vom Initiator starten. Beispielsweise kann der Beantworter Ereignisse an den Initiator senden. Es können jedoch keine Daten mit dem Ereignis gesendet werden. Wenn Daten vorhanden sind, die als Teil des Ereignisses gelesen werden müssen, muss der Initiator einen MTP-Befehl senden, und das Gerät kann dann Daten als Antwort auf den Befehl senden.

Eine umfassende Beschreibung von MTP finden Sie in der [MTP-Spezifikation](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Senden von MTP-Befehlen

Anwendungen können MTP-Befehle an ein Gerät senden, indem Sie die [**iportabledevice:: sendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) -Methode aufrufen. Der Befehl, der gesendet wird, hängt davon ab, ob es eine Daten Phase gibt, und ob alle zugehörigen Daten aus dem Gerät gelesen oder auf das Gerät geschrieben werden. In der folgenden Tabelle werden die drei möglichen MTP-Erweiterungs Befehle beschrieben.

Beachten Sie, dass diese Befehle für MTP spezifisch sind. und werden daher nur vom WPD-MTP-Klassen Treiber implementiert.



|                                                                                                                                      |                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Get-Help                                                                                                                              | BESCHREIBUNG                                                                                       |
| [**WPD- \_ Befehl \_ MTP \_ Ext \_ Ende \_ Daten \_ Übertragung**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Gibt einen MTP-Befehl aus, der das Ende eines Lese-oder Schreibvorgangs für Daten signalisiert.              |
| [**WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ ohne \_ Daten \_ Phase**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Gibt einen MTP-Befehl ohne entsprechende Daten Phase aus.                                         |
| [**WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ \_ zu schreibende Daten \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Gibt einen MTP-Befehl aus, auf den begleitende Daten folgen, die auf das Gerät geschrieben werden. |
| [**WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ \_ zu \_ lesenden Daten**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Gibt einen MTP-Befehl aus, auf den begleitende Daten folgen, die vom Gerät gelesen werden.       |
| [**WPD- \_ Befehl \_ MTP \_ Ext \_ \_ Daten lesen**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Gibt einen MTP-Befehl aus, der Daten vom Gerät an den PC sendet.                                  |
| [**WPD- \_ Befehl \_ MTP \_ Ext \_ \_ Daten schreiben**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Gibt einen MTP-Befehl aus, der vom PC Daten an das Gerät sendet.                                  |



 

Unabhängig von der Phase müssen die **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Vorgangs \_ Code** und die **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Vorgangs \_** Parameter angegeben werden.

Wenn der MTP-Treiber den Befehl an das Gerät senden konnte, enthalten die Rückgabewerte immer den **WPD- \_ \_ MTP \_ Ext- \_ Antwort \_ Code**. Wenn der Antwort Code Erfolg anzeigt und die Semantik des Befehls Antwort Parameter zulässt, ist die **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ - \_ Antwort** Parameter ebenfalls verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 
