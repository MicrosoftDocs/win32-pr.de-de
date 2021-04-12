---
title: Bandbreiten Freigabe Objekt
description: Bandbreiten Freigabe Objekt
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe von Objekten
- Advanced Systems Format (ASF), Bandbreiten Freigabe von Objekten
- ASF (Advanced Systems Format), Bandbreiten Freigabe von Objekten
- Objekte, Bandbreiten Freigabe von Objekten
- Bandbreiten Freigabe, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389896"
---
# <a name="bandwidth-sharing-object"></a>Bandbreiten Freigabe Objekt

Ein Bandbreiten Freigabe Objekt wird verwendet, um anzugeben, dass zwei oder mehr Streams, unabhängig von den einzelnen Bitraten, niemals mehr als eine festgelegte Bandbreite zwischen Ihnen verwenden werden. Dabei handelt es sich um ein reines Informationsobjekt. die darin festgelegten Bitraten werden von keinem Objekt dieses SDK Programm gesteuert erzwungen.

Informationen zur Bandbreiten Freigabe sind ein optionaler Teil eines Profils. Bandbreiten Freigabe Objekte können für vorhandene Bandbreiten Freigabe Informationen in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen. Bandbreiten Freigabe Objekte können nicht unabhängig von einem Profil Objekt vorhanden sein. Zum Speichern des Inhalts eines Bandbreiten Freigabe Objekts müssen Sie [**IWMProfile3:: addbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)abrufen.

Rufen Sie eine der folgenden Methoden auf, um ein Bandbreiten Freigabe Objekt zu erstellen.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3:: kreatenewbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Erstellt ein Bandbreiten Freigabe Objekt ohne Daten.                                                                                                           |
| [**IWMProfile3:: getbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Erstellt ein Bandbreiten Freigabe Objekt, das mit Daten aus einem Profil aufgefüllt ist. Verwendet den Bandbreiten Freigabe Index, um die gewünschten Informationen zur Bandbreiten Freigabe zu identifizieren. |



 

Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmbandwidthsharing** -Schnittstelle fest. Die **iwmstreamlist** -Schnittstelle wird von **iwmbandwidthsharing** geerbt, sodass keine **QueryInterface** mit diesem Objekt aufgerufen werden muss.

Die folgenden Schnittstellen werden von jedem Bandbreiten Freigabe Objekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**Iwmbandwidthsharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Verwaltet die Eigenschaften einer Gruppe von Streams, die Bandbreite gemeinsam nutzen. |
| [**Iwmstreamlist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Verwaltet die Liste der Streams, die Bandbreite gemeinsam nutzen.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bandbreiten Freigabe**](bandwidth-sharing.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Profil Objekt**](profile-object.md)
</dt> </dl>

 

 




