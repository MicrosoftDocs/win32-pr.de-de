---
title: Erhalten und Festlegen von Metadaten und Attributen
description: Erhalten und Festlegen von Metadaten und Attributen
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media-Device Manager, Attribute
- Device Manager, Attribute
- Desktop Anwendungen, Attribute
- Dienstanbieter, Attribute
- Programmier Handbuch, Attribute
- attributes
- Windows Media-Device Manager, Metadaten
- Device Manager, Metadaten
- Desktop Anwendungen, Metadaten
- Dienstanbieter, Metadaten
- Programmier Handbuch, Metadaten
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856351"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Erhalten und Festlegen von Metadaten und Attributen

Eine Anwendung kann zwei Arten von Informationen über einen Speicher oder ein Gerät erhalten: Attribute und Metadaten. Attribute sind einfachere boolesche Werte, die in der Regeldatei Systeminformationen beschreiben, z. b. ob ein Speicher über untergeordnete Objekte verfügt, ob er umbenannt, gelesen oder gelöscht werden kann usw. Attribute werden durch den Aufruf von [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) oder [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)als Flags-Werte abgerufen. Attribute werden durch Aufrufen von [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)festgelegt.

Eine Anwendung kann auch komplexere Daten (numerisch, Zeichenfolge oder andere Datentypen) als *Metadaten* anfordern. Metadatenwerte werden durch eindeutige Zeichen folgen Namen identifiziert. Windows Media Device Manager definiert eine Liste von Zeichen folgen Konstanten, die verwendet werden können, um Werte anzufordern. Diese definierten Werte sind unter [metadatenkonstanten](metadata-constants.md)aufgeführt. Ein Dienstanbieter kann seine eigenen Konstanten definieren, aber eine aufrufende Anwendung muss diese Definitionen beachten, um diese benutzerdefinierten Metadatenwerte anzufordern oder festzulegen. Die Anwendung fordert Metadaten durch Aufrufen von [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)an.

Ein wichtiger Aspekt beim Abrufen und Festlegen von Metadaten und Attributen besteht darin, zu verstehen, woher die abgerufenen Werte stammen. Der Dienstanbieter oder das Gerät kann diese Werte von vielen verschiedenen Orten erhalten, einschließlich der folgenden:

-   Aus dem Dateiheader. In einer ASF-Datei wird die Bitrate z. b. im Dateiheader gespeichert.
-   Aus Werten, die explizit von der Anwendung festgelegt werden, wenn eine Methode aufgerufen wird. Diese Werte können in einem externen Metadatenspeicher im Dienstanbieter oder auf dem Gerät gespeichert werden. Dieser Speicher kann beibehalten werden, wenn das Gerät die Verbindung trennt oder ausgeschaltet wird. Beispielsweise werden der Wert für die Wiedergabe Anzahl und die Benutzer Sterne in der Regel in externen Stores auf dem Computer oder auf dem Gerät gespeichert.
-   Durch Untersuchen von Informationen, die vom Dateisystem bereitgestellt werden. Beispielsweise, ob eine Datei schreibgeschützt ist oder ob ein Ordner über untergeordnete Elemente verfügt.
-   Durch Öffnen und übernehmen der Datei Daten.

Es ist wichtig zu wissen, dass eine Eigenschaft möglicherweise an mehr als einem Speicherort (innerhalb des Datei Headers und auch in einem lokalen Speicher) gespeichert wird und dass Sie bearbeitet werden kann oder nicht. Beispielsweise kann es sein, dass das Ändern einer Dateibeschreibung persistent ist. Wenn der Dienstanbieter die Beschreibung lokal speichert, wird er nicht auf dem Gerät gespeichert. Ebenso gilt: Wenn die Dateibeschreibung aus dem Dateiheader entnommen wird, ist eine Änderung der Datei nur persistent, wenn der Dienstanbieter oder das Gerät geöffnet wird und die Header Daten ändert. Die meisten Anwendungen haben einen optimalen Versuch, wenn Sie die gewünschten Werte ändern, aber nicht davon abhängen, dass Eigenschaften permanent geändert werden.

Weitere Informationen zum erhalten und Festlegen von Werten finden Sie in den entsprechenden Abschnitten für Anwendungsentwickler und Dienstanbieter Entwickler später in der-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




