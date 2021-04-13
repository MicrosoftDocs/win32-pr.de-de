---
title: Zugreifen auf Metadaten und Attribute in der APP
description: Erhalten und Festlegen von Metadaten und Attributen in der Anwendung
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media-Device Manager, Metadaten
- Device Manager, Metadaten
- Programmier Handbuch, Metadaten
- Desktop Anwendungen, Metadaten
- Erstellen von Windows Media Device Manager-Anwendungen, Metadaten
- metadata
- Windows Media-Device Manager, Attribute
- Device Manager, Attribute
- Programmier Handbuch, Attribute
- Desktop Anwendungen, Attribute
- Erstellen von Windows Media Device Manager-Anwendungen, Attributen
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313853"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Zugreifen auf Metadaten und Attribute in der APP

Eine allgemeine Erläuterung der Metadaten und Attribute finden Sie unter [erhalten und Festlegen von Metadaten und Attributen](getting-and-setting-metadata-and-attributes.md). In diesem Abschnitt werden bestimmte Anwendungsmethoden Aufrufe zum Abrufen oder Festlegen von Werten behandelt.

Anwendungen können Attribute oder Metadaten zu einem bestimmten Speicher abrufen, indem Sie [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)aufrufen. **GetMetadata** Ruft eine vollständige Auflistung aller Metadaten ab, die einem Speicher zugeordnet sind, und die Anwendung kann dann alle Werte durchlaufen oder bestimmte Werte aus der Sammlung anfordern. **Getspecifiedmetadata** erstellt im Namen des Aufrufers ein Metadatenobjekt. Der Aufrufer kann eine Teilmenge der verfügbaren Daten anfordern, indem er den *ppwszpropnames* -Parameter mit einem Array der gewünschten Eigenschaften Zeichenfolgen für Windows Media Device Manager und die Anzahl dieses Arrays abfüllt. Das zurückgegebene Metadatenobjekt wird mit den Eigenschaften aufgefüllt, die abgerufen werden können. Die Eigenschaften, die nicht abgerufen werden konnten, sind nicht vorhanden. Metadaten werden auf Grundlage der bestmöglichen Leistung zurückgegeben.

Ein Gerät kann Attribute oder Metadaten für einen Speicher durch Aufrufen von [**iwmdmstorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)oder [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)festlegen. Beachten Sie, dass es keine Garantie gibt, dass die festgelegten Werte beibehalten werden, da Sie möglicherweise in einem nicht persistenten externen Dateispeicher gespeichert werden. die Werte werden möglicherweise nicht unterstützt, oder das Gerät unterstützt die Eigenschaften möglicherweise nicht als beschreibbar.

Sie können auch Metadaten zu einem Gerät abrufen oder festlegen, indem Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) oder [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty)aufrufen. Am Ende der [metadatenkonstanten](metadata-constants.md)ist eine separate Tabelle mit gerätemetadatenkonstanten aufgeführt.

Beispiele für die Verwendung dieser Methoden finden Sie in der Referenz Dokumentation jeder Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Erhalten und Festlegen von Metadaten und Attributen**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




