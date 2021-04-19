---
description: Logische Sensoren stellen Daten ohne abhängig von Hardware Geräten bereit.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Informationen zu logischen Sensoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362631"
---
# <a name="about-logical-sensors"></a>Informationen zu logischen Sensoren

*Logische Sensoren* stellen Daten ohne abhängig von Hardware Geräten bereit. Ein logischer Sensor könnte z. b. Daten über den aktuellen Speicherort des Benutzers bereitstellen, indem er einen Dienst verwendet, der eine IP-Adresse in einer Tabelle nach sucht. Logische Sensoren werden als Sensor Treiber implementiert. Informationen zum Implementieren eines Sensor Treibers finden Sie im Windows-Treiberkit.

Nachdem ein logischer Sensor auf dem Computer des Benutzers installiert wurde, können Sie ihn auf dieselbe Weise wie einen hardwarebasierten Sensor verwenden. Die Sensor-API stellt eine [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle bereit, um den logischen Sensor darzustellen, und das Programm kann Daten über die gleichen Mechanismen anfordern, die Sie für jeden anderen Sensortyp verwenden würden. Logische Sensoren können auch Platt Form definierte Sensor Kategorien,-Typen,-Datentypen,-Eigenschaften und-Ereignisse verwenden. Oder Sie können benutzerdefinierte Werte definieren.

Mithilfe der [**ilogicalsensormanager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) -Schnittstelle können Entwickler, die logische Sensoren erstellen, Verbindungen mit der Sensor-und der Location-Plattform verwalten.

> [!Note]  
> Wie bei anderen Treibern erfordert das Installieren oder Deinstallieren eines logischen Sensor Treibers Administratorrechte.

 

Weitere Informationen zum Verwenden eines logischen Beispiel Sensors finden Sie unter [Informationen zu den Beispielen und Tools](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Verwalten logischer Sensoren

[**Ilogicalsensormanager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) verfügt über die folgenden Methoden:

-   [**Verbinden**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Trennen**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Deinstallieren**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Wenn Sie [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))aufgerufen haben, erstellt die Sensor-API eine Instanz des Sensor Treibers, sofern noch keine vorhanden ist, und verbindet dann den logischen Sensor mit der Plattform. Dies bedeutet, dass der logische Sensor mit anderen Sensoren in der Systemsteuerung **Standort und andere Sensoren** angezeigt wird. Wenn Sie die Verbindung [**trennen**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), trennt die Sensor-API den logischen Sensor und entfernt ihn aus der Systemsteuerung. Durch den Aufruf von **Disconnect** wird der logische Sensor nicht aus **Device Manager** entfernt. Folglich führen zukünftige Aufrufe von **Connect** zu einer viel schnelleren Verbindung mit dem logischen Sensor.

Zum Entfernen eines logischen Sensors müssen Sie [**deinstallieren**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). Durch die Deinstallation eines logischen Sensors wird der Sensor aus **Device Manager** entfernt. Da logische Sensorgeräte nur im Arbeitsspeicher vorhanden sind, wird ein logischer Sensor deinstalliert, wenn der Benutzer Windows neu startet.

Die Sensor-API identifiziert einen bestimmten logischen Sensor anhand seiner *logischen ID*, bei der es sich um eine **GUID** handelt. Jedes Mal, wenn Sie eine Verbindung mit einem bestimmten logischen Sensor herstellen, müssen Sie eine logische ID angeben. Jedes Mal, wenn Sie einen bestimmten Sensor trennen oder deinstallieren, müssen Sie die gleiche logische ID angeben, die Sie zum Herstellen der Verbindung verwendet haben. Wenn Sie mithilfe verschiedener logischer IDs mehrmals eine Verbindung mit demselben logischen Sensor Treiber herstellen, erstellen Sie für jede neue logische ID eine separate Instanz des logischen Sensors. Auch wenn Sie für jede logische ID die Verbindung [**trennen**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) , verbleiben diese separaten Instanzen **Device Manager** , bis Sie für jeden logischen Sensor [**deinstallieren**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) oder Windows neu startet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden logischer Sensoren](using-logical-sensors.md)
</dt> </dl>

 

 
