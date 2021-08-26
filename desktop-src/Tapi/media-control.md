---
description: Das Medium einer Kommunikationssitzung ist das Format, in dem die Daten übertragen werden. Mediensteuerelemente ermöglichen es einer Anwendung, eine Vielzahl von Medientypen zu erkennen und Aspekte des Mediendatenstroms anzupassen, z. B. die Lautstärke der Sprachübertragung.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Mediensteuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e3ad30107a98cc5d1a312880fa29422c42dce2b2bc59cadfbf894cb032d74a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034530"
---
# <a name="media-control"></a>Mediensteuerelement

Das Medium einer Kommunikationssitzung ist das Format, in dem die Daten übertragen werden. Mediensteuerelemente ermöglichen es einer Anwendung, eine Vielzahl von Medientypen zu erkennen und Aspekte des Mediendatenstroms anzupassen, z. B. die Lautstärke der Sprachübertragung.

Die Verfügbarkeit von Mediensteuerung und -informationen variiert je nach Typ der TAPI-Anwendung, Dienstanbieterunterstützung und der lokalen Kommunikationsumgebung stark. Das folgende Material enthält eine allgemeine Beschreibung des Mediensteuerelements. TAPI bietet ein flexibles Framework für die Implementierung von Steuerelementen, sodass die interessantsten Funktionen häufig für einen bestimmten Dienstanbieter spezifisch sind.

Bei der klassischen Telefonie hatte eine Anwendung nur sehr wenig Kontrolle über den Mediendatenstrom, nachdem ein Kommunikationspfad eingerichtet wurde. TAPI 2-Anwendungen haben Zugriff auf einige Funktionen, die es ihnen ermöglichen, Ziffern oder Töne während eines Aufrufs zu erkennen und darauf zu reagieren, und sie können die Wave-API verwenden, um während einer Kommunikationssitzung zusätzliche Kontrolle über Medien zu haben, aber andernfalls haben sie keinen Medienstreamzugriff. Eine Überprüfung dieser Funktionen finden Sie in der Übersicht über TAPI 2.2 [Media Access](./media-access.md) oder in der Übersicht über DEN [TSPI-Medienzugriff.](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85))

TAPI 3 führt die [Mediendienstanbieter ein,](about-the-media-service-provider-msp-.md)die sowohl Informationen zu als auch die Kontrolle über die Medien oder eine Kommunikationssitzung deutlich erhöhen. Eine TAPI 3-Anwendung kann direkt auf den [Medienstream](stream-objects.md) einer Sitzung zugreifen. Für jeden Medientyp, der an der Sitzung beteiligt ist, wird ein separater Stream erstellt, z. B. Sprach- oder Videodatenstrom. Einige MSPs implementieren möglicherweise Unterstreamsteuerelemente, die Streams weiter unterteilen können, z. B. nach Teilnehmer im Fall des IPConf-MSP.



| TAPI 2.x-Funktionen                                          | BESCHREIBUNG                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Initiiert das gepufferte Sammeln von Ziffern für den angegebenen Aufruf.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Initiiert die Generierung der angegebenen Ziffern für den angegebenen Aufruf als Inbandfarben unter Verwendung des angegebenen Signalisierungsmodus. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Generiert den angegebenen Inbandton über dem angegebenen Aufruf.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Aktiviert und deaktiviert die ungepufferte Erkennung von Ziffern, die beim Aufruf empfangen wurden.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Aktiviert und deaktiviert die Erkennung von Medientypen für den angegebenen Aufruf.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Aktiviert und deaktiviert die Erkennung von Inbandfarben beim Aufruf.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Aktiviert und deaktiviert Steuerungsaktionen für den Medienstream, der der angegebenen Zeile, Adresse oder dem angegebenen Aufruf zugeordnet ist.             |



 



| TAPI 3.x-Schnittstellen oder -Methoden                               | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Unterstützt Legacyanwendungen, die direkt mit einem Gerät kommunizieren müssen.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Ermöglicht einer Anwendung zu ermitteln, ob ein von einem Legacy-TSP (pre-TAPI 3) erstelltes Terminal mithilfe der Wave-API gesteuert werden kann.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Ermöglicht einer Anwendung das Abrufen von Informationen in einem Stream. , um den Stream zu starten, anzuhalten oder zu beenden; , um Terminals in einem Stream auszuwählen oder die Auswahl aufzuheben; und , um eine Liste der im Stream ausgewählten Terminals abzurufen. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Ermöglicht einer Anwendung das Aufzählen, Erstellen oder Entfernen von Medienstreams.                                                                                                                                   |



 

 

 
