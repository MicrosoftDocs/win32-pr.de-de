---
description: Unterstützen von MTP-Erweiterungen
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Unterstützen von MTP-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898df3f1347af2ccc42a796b480156b6603b13ec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423730"
---
# <a name="supporting-mtp-extensions"></a>Unterstützen von MTP-Erweiterungen

## <a name="media-transfer-protocol"></a>Medienübertragungsprotokoll

Das Media Transfer Protocol (MTP) ist eine Erweiterung des Picture Transfer Protocol (PTP). Daher sind alle PTP-Protokollsemantiken in MTP gültig.

MTP kommuniziert mithilfe von Befehlen und Antworten zwischen zwei Parteien, dem Initiator und dem Beantworter. Die Rollen der beteiligten Geräte sind sehr klar definiert. Der PC ist in der Regel der Initiator, und das Gerät ist immer der Antworter. Ein Nicht-PC-Gerät kann auch ein Initiator sein (z. B. ein Autostapel oder eine Microsoft X-Box). Ein Gerät kann nie beide Rollen gleichzeitig übernehmen.

Der Initiator startet die Kommunikation, indem er einen Befehl an den Antworter sendet. Der Antworter verarbeitet den Befehl und sendet eine entsprechende Antwort zurück. Dem Befehl kann eine Datenphase zugeordnet sein. Wenn dies der Fall ist, muss die Richtung des Datenflusses im Voraus bekannt sein und sowohl vom Initiator als auch vom Antworter akzeptiert werden. Beachten Sie, dass es keinen beschreibenden Header gibt, der Datenflüsse für neue Befehle angibt.

Der Beantworter kann die Kommunikation unabhängig vom Initiator starten. Beispielsweise kann der Beantworter Ereignisse an den Initiator senden. Es können jedoch keine Daten zusammen mit dem Ereignis gesendet werden. Wenn Daten im Rahmen des Ereignisses gelesen werden müssen, muss der Initiator einen MTP-Befehl senden, und das Gerät kann dann daten als Reaktion auf den Befehl senden.

Eine vollständige Beschreibung von MTP finden Sie in der [MTP-Spezifikation.](https://www.usb.org/sites/default/files/MTPv1_1.zip)

## <a name="sending-mtp-commands"></a>Senden von MTP-Befehlen

Anwendungen können MTP-Befehle an ein Gerät senden, indem sie die [**IPortableDevice::SendCommand-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) aufrufen. Der gesendete Befehl hängt davon ab, ob es eine Datenphase gibt und ob zugehörige Daten vom Gerät gelesen oder auf das Gerät geschrieben werden. In der folgenden Tabelle werden die drei möglichen MTP-Erweiterungsbefehle beschrieben.

Beachten Sie, dass diese Befehle für MTP spezifisch sind. und werden daher nur vom WPD MTP-Klassentreiber implementiert.



| Befehl  | BESCHREIBUNG  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WPD-BEFEHL \_ \_ MTP \_ EXT END \_ DATA \_ \_ TRANSFER**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Gibt einen MTP-Befehl aus, der den Abschluss eines Datenlese- oder -schreibvorganges signalisiert.              |
| [**WPD-BEFEHL \_ \_ MTP \_ EXT BEFEHL OHNE \_ \_ \_ \_ DATENPHASE \_ AUSFÜHREN**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Gibt einen MTP-Befehl ohne eine entsprechende Datenphase aus.                                         |
| [**WPD-BEFEHL \_ \_ MTP \_ EXT \_ \_ EXECUTE-BEFEHL \_ MIT ZU \_ \_ SCHREIBENDEN \_ DATEN**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Gibt einen MTP-Befehl aus, auf den begleitende Daten folgen, die auf das Gerät geschrieben werden. |
| [**WPD-BEFEHL \_ \_ MTP \_ EXT \_ \_ EXECUTE-BEFEHL \_ MIT ZU \_ \_ LESENDEN \_ DATEN**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Gibt einen MTP-Befehl aus, auf den begleitende Daten folgen, die vom Gerät gelesen werden.       |
| [**WPD-BEFEHL \_ \_ MTP \_ EXT READ \_ \_ DATA**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Gibt einen MTP-Befehl aus, der Daten vom Gerät an den PC sendet.                                  |
| [**WPD-BEFEHL \_ \_ MTP \_ EXT WRITE \_ \_ DATA**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Gibt einen MTP-Befehl aus, der Daten vom PC an das Gerät sendet.                                  |



 

Unabhängig von der Phase müssen **WPD \_ PROPERTY \_ MTP \_ EXT OPERATION \_ \_ CODE** und **WPD PROPERTY \_ \_ MTP EXT OPERATION \_ \_ \_ PARAMS** angegeben werden.

Wenn der MTP-Treiber den Befehl an das Gerät senden konnte, enthalten die Rückgabewerte immer **WPD \_ PROPERTY \_ MTP \_ EXT RESPONSE \_ \_ CODE**. Wenn der Antwortcode den Erfolg angibt und die Semantik des Befehls Antwortparameter zulässt, ist **WPD \_ PROPERTY \_ MTP \_ EXT RESPONSE \_ \_ PARAMS** ebenfalls verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 
