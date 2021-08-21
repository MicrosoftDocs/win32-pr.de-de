---
description: Logische Sensoren stellen Daten ohne Abhängigkeit von Hardwaregeräten bereit.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Informationen zu logischen Sensoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bb7a6e67223bb959b155e55f6cc059ffd8280bc8c08fb00d4d88cb2c8b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003892"
---
# <a name="about-logical-sensors"></a>Informationen zu logischen Sensoren

*Logische Sensoren* stellen Daten ohne Abhängigkeit von Hardwaregeräten bereit. Beispielsweise kann ein logischer Sensor Daten zum aktuellen Standort des Benutzers bereitstellen, indem er einen Dienst verwendet, der eine IP-Adresse in einer Tabelle sucht. Logische Sensoren werden als Sensortreiber implementiert. Informationen zum Implementieren eines Sensortreibers finden Sie im Windows Driver Kit.

Nachdem ein logischer Sensor auf dem Computer des Benutzers installiert wurde, können Sie ihn auf die gleiche Weise wie einen hardwarebasierten Sensor verwenden. Die Sensor-API stellt eine [**ISensor-Schnittstelle**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) bereit, die den logischen Sensor darstellt, und Ihr Programm kann Daten über die gleichen Mechanismen anfordern, die Sie für jeden anderen Sensortyp verwenden würden. Logische Sensoren können auch die plattformdefinierte Sensorkategorien, -typen, -datentypen, -eigenschaften und -ereignisse verwenden. Sie können auch benutzerdefinierte Werte definieren.

Mit der [**ILogicalSensorManager-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) können Entwickler, die logische Sensoren erstellen, Verbindungen mit der Sensor and Location-Plattform verwalten.

> [!Note]  
> Wie bei anderen Treibern sind für die Installation oder Deinstallation eines logischen Sensortreibers Administratorrechte erforderlich.

 

Informationen zur Verwendung eines logischen Beispielsensors finden Sie unter [Informationen zu Beispielen und Tools.](about-the-samples.md)

## <a name="managing-logical-sensors"></a>Verwalten logischer Sensoren

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) verfügt über die folgenden Methoden:

-   [**Verbinden**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Trennen**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Deinstallieren**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Wenn Sie [**Verbinden**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))aufrufen, erstellt die Sensor-API eine Instanz des Sensortreibers, sofern noch nicht vorhanden, und verbindet dann den logischen Sensor mit der Plattform. Dies bedeutet, dass der logische Sensor mit anderen Sensoren im **Positions- und andere Sensoren** Systemsteuerung angezeigt wird. Wenn Sie [**Trennen**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))aufrufen, trennt die Sensor-API den logischen Sensor und entfernt ihn aus dem Systemsteuerung. Wenn **Sie Disconnect** aufrufen, wird der logische Sensor nicht aus **Geräte-Manager** entfernt. Daher führen zukünftige Aufrufe von **Verbinden** zu einer viel schnelleren Verbindung mit dem logischen Sensor.

Um einen logischen Sensor zu entfernen, müssen Sie [**Deinstallieren**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))aufrufen. Durch das Deinstallieren eines logischen Sensors wird der Sensor aus **Geräte-Manager** entfernt. Da logische Sensorgeräte nur im Arbeitsspeicher vorhanden sind, wird ein logischer Sensor deinstalliert, wenn der Benutzer Windows neu startet.

Die Sensor-API identifiziert einen bestimmten logischen Sensor anhand seiner *logischen ID*, bei der es sich um eine **GUID** handelt. Jedes Mal, wenn Sie eine Verbindung mit einem bestimmten logischen Sensor herstellen, müssen Sie eine logische ID angeben. Jedes Mal, wenn Sie einen bestimmten Sensor trennen oder deinstallieren, müssen Sie dieselbe logische ID angeben, die Sie zum Herstellen der Verbindung verwendet haben. Wenn Sie mehrmals über verschiedene logische IDs eine Verbindung mit demselben logischen Sensortreiber herstellen, erstellen Sie eine separate Instanz des logischen Sensors für jede neue logische ID. Selbst wenn Sie [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) für jede logische ID aufrufen, bleiben diese separaten Instanzen in **Geräte-Manager,** bis Sie [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) für jeden logischen Sensor aufrufen oder der Benutzer Windows neu startet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden logischer Sensoren](using-logical-sensors.md)
</dt> </dl>

 

 
