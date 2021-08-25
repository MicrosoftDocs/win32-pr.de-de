---
title: Abrufen und Festlegen von Metadaten und Attributen
description: Abrufen und Festlegen von Metadaten und Attributen
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Medien Geräte-Manager,Attribute
- Geräte-Manager,Attribute
- Desktopanwendungen,Attribute
- Dienstanbieter,Attribute
- Programmierhandbuch,Attribute
- attributes
- Windows Medien Geräte-Manager,Metadaten
- Geräte-Manager,metadata
- Desktopanwendungen,Metadaten
- Dienstanbieter,Metadaten
- Programmierhandbuch,Metadaten
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c8311c3fff3c4785116604e53652c4f07b6b63b3a2c4389cc3dd4b6a5f35a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957560"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Abrufen und Festlegen von Metadaten und Attributen

Eine Anwendung kann zwei Arten von Informationen zu einem Speicher oder Gerät abrufen: Attribute und Metadaten. Attribute sind einfachere boolesche Werte, die in der Regel Dateisysteminformationen beschreiben, z. B. ob ein Speicher über untergeordnete Objekte verfügt, ob er umbenannt, gelesen oder gelöscht werden kann, und so weiter. Attribute werden durch Aufrufen von [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) oder [**IWMDMStorage2::GetAttributes2 als Flagwerte abgerufen.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2) Attribute werden durch Aufrufen von [**IWMDMStorage3::SetMetadata festgelegt.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)

Eine Anwendung kann auch komplexere Daten (numerisch, Zeichenfolge oder andere Datentypen) als Metadaten *anfordern.* Metadatenwerte werden durch eindeutige Zeichenfolgennamen identifiziert. Windows Media Geräte-Manager definiert eine Liste von Zeichenfolgenkonst constants, die zum Anfordern von Werten verwendet werden können. diese definierten Werte sind unter [Metadatenkonst constants aufgeführt.](metadata-constants.md) Ein Dienstanbieter kann eigene Konstanten definieren, aber eine aufrufende Anwendung muss diese Definitionen kennen, um diese benutzerdefinierten Metadatenwerte an- oder festzulegen. Die Anwendung fordert Metadaten an, indem [**sie IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4::GetSpecifiedMetadata aufruft.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)

Ein wichtiger Aspekt beim Abrufen und Festlegen von Metadaten und Attributen ist das Verständnis, woher die abgerufenen Werte stammen. Der Dienstanbieter oder das Gerät kann diese Werte von vielen verschiedenen Orten erhalten, einschließlich der folgenden:

-   Aus dem Dateiheader. Beispielsweise wird in einer ASF-Datei die Bitrate im Dateiheader gespeichert.
-   Aus Werten, die beim Aufrufen einer Methode explizit von der Anwendung festgelegt werden. Diese Werte können in einem externen Metadatenspeicher im Dienstanbieter oder auf dem Gerät gespeichert werden. Dieser Speicher kann beibehalten werden, wenn das Gerät getrennt oder ausgeschaltet wird. Beispielsweise werden die Wiedergabeanzahl und die Benutzer-Sternbewertungen in der Regel in externen Speichern auf dem Computer oder Gerät gespeichert.
-   Durch Untersuchen der vom Dateisystem bereitgestellten Informationen. Beispielsweise, ob eine Datei schreibgeschützt ist oder ob ein Ordner über children verfügt.
-   Durch Öffnen und Analyse der Dateidaten.

Es ist wichtig zu wissen, dass eine Eigenschaft an mehr als einem Speicherort (innerhalb des Dateiheaders und auch in einem lokalen Speicher) gespeichert werden kann und dass sie möglicherweise bearbeitet werden kann. Das Ändern einer Dateibeschreibung kann z. B. persistent sein. Wenn der Dienstanbieter die Beschreibung lokal speichert, wird sie nicht auf dem Gerät beibehalten. Wenn die Dateibeschreibung aus dem Dateiheader übernommen wird, ist eine Änderung nur dann persistent, wenn der Dienstanbieter oder das Gerät geöffnet wird und die Headerdaten ändert. Die meisten Anwendungen versuchen am besten, die gewünschten Werte zu ändern, hängen jedoch nicht davon ab, dass Eigenschaften dauerhaft geändert werden.

Weitere Informationen zum Abrufen und Festlegen von Werten finden Sie in den entsprechenden Abschnitten für Anwendungsentwickler und Dienstanbieterentwickler weiter unten in der Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




