---
title: Objekt für die Bandbreitenfreigabe
description: Objekt für die Bandbreitenfreigabe
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Medienformat-SDK, Objekte für die Bandbreitenfreigabe
- Advanced Systems Format (ASF), Bandbreitenfreigabeobjekte
- ASF (Advanced Systems Format), Bandbreitenfreigabeobjekte
- Objekte, Objekte mit Bandbreitenfreigabe
- Bandbreitenfreigabe, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 449a1e43a8f5c7212f1e9c4240d85eb11c9ee39209fab4313b373a56d017b2dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055600"
---
# <a name="bandwidth-sharing-object"></a>Objekt für die Bandbreitenfreigabe

Ein Bandbreitenfreigabeobjekt wird verwendet, um anzugeben, dass zwei oder mehr Datenströme unabhängig von ihren einzelnen Bitraten nie mehr als eine angegebene Bandbreite zwischen ihnen verwenden. Dies ist ein reines Informationsobjekt. Die darin festgelegten Bitraten werden von keinem Objekt dieses SDK programmgesteuert erzwungen.

Informationen zur Bandbreitenfreigabe sind ein optionaler Teil eines Profils. Objekte für die Bandbreitenfreigabe können für vorhandene Informationen zur Bandbreitenfreigabe in einem Profil erstellt oder leer erstellt werden, um neue Daten zu empfangen. Objekte für die Bandbreitenfreigabe können nicht unabhängig von einem Profilobjekt vorhanden sein. Um den Inhalt eines Bandbreitenfreigabeobjekts zu speichern, müssen Sie [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)aufrufen.

Um ein Objekt für die Bandbreitenfreigabe zu erstellen, rufen Sie eine der folgenden Methoden auf.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Erstellt ein Bandbreitenfreigabeobjekt ohne Daten.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Erstellt ein Bandbreitenfreigabeobjekt, das mit Daten aus einem Profil aufgefüllt wird. Verwendet den Index für die Bandbreitenfreigabe, um die gewünschten Informationen zur Bandbreitenfreigabe zu identifizieren. |



 

Beide Methoden in der obigen Tabelle legen einen Zeiger auf eine **IWMBandwidthSharing-Schnittstelle** fest. Die **IWMStreamList-Schnittstelle** wird von **IWMBandwidthSharing** geerbt, sodass **queryInterface** nicht mit diesem Objekt aufgerufen werden muss.

Die folgenden Schnittstellen werden von jedem Objekt für die Bandbreitenfreigabe unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Verwaltet die Eigenschaften einer Gruppe von Datenströmen, die die Bandbreite gemeinsam nutzen. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Verwaltet die Liste der Streams, die die Bandbreite gemeinsam nutzen.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bandbreitenfreigabe**](bandwidth-sharing.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Profilobjekt**](profile-object.md)
</dt> </dl>

 

 




