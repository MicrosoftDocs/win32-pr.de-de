---
description: Das Windows SDK enthält nützliche Codebeispiele und Tools, mit deren Hilfe Sie die Windows Sensor- und Standortplattform und die zugehörigen APIs verstehen und verwenden können.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Informationen zu den Beispielen und Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890319"
---
# <a name="about-the-samples-and-tools"></a>Informationen zu den Beispielen und Tools

Das Windows SDK enthält nützliche Codebeispiele und Tools, mit deren Hilfe Sie die Windows Sensor- und Standortplattform und die zugehörigen APIs verstehen und verwenden können.

## <a name="samples"></a>Beispiele

Das Windows SDK enthält die folgenden Sensor-API-Beispiele. Sie finden die Sensor-API-Beispiele im Ordner Samples winui Sensors, in dem Sie das Windows \\ \\ INSTALLIERT \\ haben. Wenn Sie beispielsweise das Windows SDK auf Laufwerk C installiert haben, finden Sie die Beispiele im folgenden Ordner: C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ winui \\ Sensors.



| Name des Beispiels       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Dieses MFC-Beispiel zeigt, wie Sie die Sensor-API verwenden, indem Sie Daten von Umgebungslichtsensoren auf dem Computer lesen und die Textgröße entsprechend den Beleuchtungsbedingungen ändern. Sie können Code sehen, der zeigt, wie Ereignisse verwaltet und Benutzerberechtigungen anfordern. Sie können auch ein Beispiel für die Verwaltung der Benutzeroberfläche basierend auf unterschiedlichen Beleuchtungsbedingungen sehen. Weitere Informationen finden Sie unter [Erstellen Light-Aware Benutzeroberflächen.](creating-light-aware-user-interfaces.md)<br/> Sie müssen Visual Studio 2008 installiert haben, um dieses Beispiel zu erstellen.<br/> |



 

Weitere Informationen finden Sie in der Datei namens ReadMe.txt, die im Beispiel enthalten ist.

Sie können auch das AmbientLightAware-Beispiel aus dem Codekatalog herunterladen. Weitere Informationen finden Sie auf der [Downloadseite Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Tools

Das Windows SDK enthält einen virtuellen Lichtsensor, mit dem Sie ein hardwarebasiertes Lichtsensorgerät simulieren können. Sie können dieses Tool verwenden, um Daten für das AmbientLightAware-Beispiel zur Verfügung zu stellen, um zu sehen, wie der Code im Beispiel funktioniert.

In der folgenden Tabelle werden die Dateien beschrieben, die Sie zum Ausführen des virtuellen Lichtsensors verwenden müssen. Sie finden diese Dateien im Ordner Bin, in dem Sie das Windows INSTALLIERT haben. Wenn Sie beispielsweise das Windows SDK auf Laufwerk C auf einem 32-Bit-Computer installiert haben, befinden sich die Dateien des virtuellen Lichtsensors im folgenden Ordner: C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Bin. Auf 64-Bit-Computern müssen Sie die 64-Bit-Version des Tools verwenden. Im Windows SDK befinden sich 64-Bit-Tools im Unterordner x64.



| Dateiname                    | BESCHREIBUNG                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Dieses Programm bietet ein Schieberegler-Steuerelement, mit dem Sie die Ebene der lichten Daten ändern können, die der virtuelle Sensor meldet. |
| VirtualLightSensorDriver.dll | Der logische Sensortreiber, der einen Lichtsensor simuliert.                                                                       |
| VirtualLightSensorDriver.inf | Die INF-Datei für den Virtuellen Lichtsensortreiber.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Installieren des virtuellen Lichtsensors

Bevor Sie die Anwendung für den virtuellen Lichtsensor verwenden, müssen Sie den logischen Sensortreiber installieren. Folgen Sie diesen Schritten:

1.  Öffnen Sie ein Befehlsfenster als Administrator.
2.  Wechseln Sie zum Ordner Windows SDK Bin.
3.  Geben **Sie pnputil -a VirtualLightSensorDriver.inf ein.**
4.  Wenn Sie dazu aufgefordert werden, klicken **Sie auf Diese Treibersoftware trotzdem installieren.**
5.  Warten Sie, bis das Befehlsfenster berichtet, dass der Treiber erfolgreich installiert wurde.

### <a name="running-the-virtual-light-sensor"></a>Ausführen des virtuellen Lichtsensors

Doppelklicken Sie zum Ausführen des virtuellen Lichtsensors einfach auf die .exe Datei. Stellen Sie sicher, dass Sie den Sensor aktivieren, wenn Sie dazu aufgefordert werden.

Wenn Sie das Programm ausführen, stellen Sie möglicherweise fest, dass es eine Verzögerung gibt, bevor der Sensor verfügbar wird. Die Benutzeroberfläche des virtuellen Lichtsensors zeigt die Meldung "Warten" in der Titelleiste an, während der logische Sensor-Manager einen Geräteknoten für den logischen Sensor erstellt. Nachdem die wartende Nachricht entfernt wurde, können Sie mit dem Schieberegler die Lux-Ausgabeebene für den virtuellen Lichtsensor festlegen.

Die folgende Abbildung zeigt die Benutzeroberfläche des virtuellen Lichtsensors im zustandsbereiten Zustand.

![Benutzeroberfläche des virtuellen Lichtsensors](images/virtuallightsensor.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu logischen Sensoren](about-logical-sensors.md)
</dt> <dt>

[**SENSORKATEGORIE \_ \_ LIGHT**](sensor-category-light.md)
</dt> </dl>

 

