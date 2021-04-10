---
description: Die Windows SDK enthält nützliche Codebeispiele und Tools, mit denen Sie die Windows-Sensor-und-Speicherort Plattform und zugehörige APIs verstehen und verwenden können.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Informationen zu den Beispielen und Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867619"
---
# <a name="about-the-samples-and-tools"></a>Informationen zu den Beispielen und Tools

Die Windows SDK enthält nützliche Codebeispiele und Tools, mit denen Sie die Windows-Sensor-und-Speicherort Plattform und zugehörige APIs verstehen und verwenden können.

## <a name="samples"></a>Beispiele

Die Windows SDK umfasst die folgenden Sensor-API-Beispiele. Sie finden die Sensor-API-Beispiele im Ordner namens \\ Samples \\ WinUI \\ Sensors, in dem Sie die Windows SDK installiert haben. Wenn Sie z. b. den Windows SDK auf Laufwerk C installiert haben, finden Sie die Beispiele im folgenden Ordner: C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ WinUI \\ Sensors.



| Name des Beispiels       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ambientlightaware | In diesem MFC-Beispiel wird gezeigt, wie Sie die Sensor-API verwenden, indem Sie Daten von Umgebungslichtsensoren auf dem Computer lesen und die Textgröße entsprechend den Beleuchtungsbedingungen ändern. Sie können Code sehen, der zeigt, wie Ereignisse verwaltet und Benutzerberechtigungen angefordert werden. Sie können auch ein Beispiel für die Verwaltung der Benutzeroberfläche basierend auf verschiedenen Beleuchtungsbedingungen sehen. Weitere Informationen finden Sie unter [erstellen Light-Aware Benutzeroberflächen](creating-light-aware-user-interfaces.md).<br/> Sie müssen Visual Studio 2008 installiert haben, um dieses Beispiel zu erstellen.<br/> |



 

Weitere Informationen finden Sie in der Datei mit dem Namen ReadMe.txt, die im Beispiel enthalten ist.

Sie können auch das Beispiel "ambientlightaware" aus der Code Gallery herunterladen. Weitere Informationen finden Sie auf der Downloadseite für [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Tools

Die Windows SDK enthält einen virtuellen Lichtsensor, mit dem Sie ein Hardware basiertes Lichtsensor Gerät simulieren können. Mit diesem Tool können Sie Daten für das Beispiel "ambientlightaware" bereitstellen, um zu sehen, wie der Code im Beispiel funktioniert.

In der folgenden Tabelle werden die Dateien beschrieben, die Sie zum Ausführen des virtuellen Lichtsensors verwenden müssen. Sie finden diese Dateien im Ordner bin, in dem Sie den Windows SDK installiert haben. Wenn Sie z. b. den Windows SDK auf Laufwerk C auf einem 32-Bit-Computer installiert haben, befinden sich die Dateien des virtuellen Lichtsensors im folgenden Ordner: C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ bin. Auf 64-Bit-Computern müssen Sie die 64-Bit-Version des Tools verwenden. Im Windows SDK befinden sich 64-Bit-Tools im Unterordner "x64".



| Dateiname                    | BESCHREIBUNG                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Dieses Programm bietet ein Schieberegler-Steuerelement, mit dem Sie die Ebene der hellen Daten ändern können, die der virtuelle Sensor meldet. |
| VirtualLightSensorDriver.dll | Der Treiber für den logischen Sensor, der einen Lichtsensor simuliert.                                                                       |
| Virtuallightsensordriver. inf | Die INF-Datei für den Treiber des virtuellen Lichtsensors.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Installieren des virtuellen Lichtsensors

Bevor Sie die Anwendung für den virtuellen Lichtsensor verwenden, müssen Sie den Treiber für den logischen Sensor installieren. Führen Sie die folgenden Schritte aus:

1.  Öffnen Sie ein Befehlsfenster als Administrator.
2.  Wechseln Sie in den Windows SDK bin-Ordner.
3.  Geben Sie **PnPUtil-a virtuallightsensordriver. inf ein**.
4.  Wenn Sie dazu aufgefordert werden, klicken Sie auf **Diese Treibersoftware trotzdem installieren**.
5.  Warten Sie, bis das Befehlsfenster meldet, dass der Treiber erfolgreich installiert wurde.

### <a name="running-the-virtual-light-sensor"></a>Ausführen des virtuellen Lichtsensors

Zum Ausführen des virtuellen Lichtsensors Doppelklicken Sie einfach auf die exe-Datei. Achten Sie darauf, den Sensor zu aktivieren, wenn Sie dazu aufgefordert werden.

Wenn Sie das Programm ausführen, bemerken Sie möglicherweise eine Verzögerung, bevor der Sensor verfügbar wird. Die Benutzeroberfläche des virtuellen Lichtsensors zeigt die Meldung "wird gewartet" in der Titelleiste an, während der logische Sensor-Manager einen Geräteknoten für den logischen Sensor erstellt. Nachdem die wartende Nachricht entfernt wurde, können Sie den Schieberegler verwenden, um die Lux-Ausgabe Ebene für den virtuellen Lichtsensor festzulegen.

In der folgenden Abbildung wird die Benutzeroberfläche des virtuellen Light-Sensors im Status bereit angezeigt.

![Benutzeroberfläche des virtuellen Lichtsensors](images/virtuallightsensor.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu logischen Sensoren](about-logical-sensors.md)
</dt> <dt>

[**Sensor \_ Kategorie \_ hell**](sensor-category-light.md)
</dt> </dl>

 

