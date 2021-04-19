---
description: Die Medien einer Kommunikationssitzung sind das Formular, in dem die Daten übertragen werden. Mit mediensteuer Elementen kann eine Anwendung eine Vielzahl von Medientypen erkennen und Aspekte des Medien Stroms anpassen, z. b. die Menge der Sprachübertragung.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Mediensteuer Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dad56e3feef8493a70cf93152b225be2777848
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361762"
---
# <a name="media-control"></a>Mediensteuer Element

Die Medien einer Kommunikationssitzung sind das Formular, in dem die Daten übertragen werden. Mit mediensteuer Elementen kann eine Anwendung eine Vielzahl von Medientypen erkennen und Aspekte des Medien Stroms anpassen, z. b. die Menge der Sprachübertragung.

Die Verfügbarkeit von Mediensteuerung und-Informationen variiert stark von der Art der TAPI-Anwendung, der Dienstanbieter Unterstützung und der lokalen Kommunikationsumgebung. Das folgende Material enthält eine allgemeine Beschreibung der Mediensteuerung. TAPI stellt ein flexibles Framework für die Implementierung von Steuerelementen bereit, sodass die interessantesten Funktionen häufig für einen bestimmten Dienstanbieter spezifisch sind.

Unter klassischer Telefonie hatte eine Anwendung nur wenig Kontrolle über den Mediendaten Strom, nachdem ein Kommunikations Pfad eingerichtet wurde. TAPI 2-Anwendungen haben Zugriff auf einige Funktionen, die es Ihnen ermöglichen, Ziffern oder Töne während eines Aufrufes zu erkennen und darauf zu reagieren. Außerdem können Sie die Wave-API verwenden, um während einer Kommunikationssitzung zusätzliche Steuerungsmöglichkeiten für Medien zu verwenden. andernfalls haben Sie keinen Zugriff auf den Mediendaten Strom. Eine Übersicht über diese Funktionen finden Sie in der Übersicht über den [Media Access](./media-access.md) für TAPI 2,2 oder in der Übersicht über den TSPI- [Medien Zugriff](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) .

TAPI 3 bietet eine Einführung in die [Media Service-Anbieter](about-the-media-service-provider-msp-.md), die sowohl Informationen über als auch die Kontrolle über die Medien oder eine Kommunikationssitzung erhöhen. Eine TAPI 3-Anwendung kann direkt auf den Mediendaten [Strom](stream-objects.md) einer Sitzung zugreifen. Für jeden Medientyp, der an der Sitzung beteiligt ist, wird ein separater Stream erstellt, z. b. sprach-oder Videodateien. Einige MSPs implementieren möglicherweise substreamsteuerelemente, die Datenströme weiter aufteilen können, z. b. durch den Teilnehmer im Fall von ipconf-MSP.



| TAPI 2. x-Funktionen                                          | BESCHREIBUNG                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**linegather-Ziffern**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Initiiert die gepufferte Erfassung von Ziffern für den angegebenen-Befehl.                                                          |
| [**linegeneratedigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Initiiert die Generierung der angegebenen Ziffern für den angegebenen-Befehl als Inband-Töne unter Verwendung des angegebenen Signal Modus. |
| [**linegeneratetone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Generiert den angegebenen Inband-Ton für den angegebenen-Befehl.                                                               |
| [**linemonitordigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Aktiviert und deaktiviert die nicht gepufferte Erkennung von Ziffern, die für den-Befehl empfangen wurden.                                              |
| [**linemonitormedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Aktiviert und deaktiviert die Erkennung von Medientypen für den angegebenen-Befehl.                                                   |
| [**linemonitortones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Aktiviert und deaktiviert die Erkennung von Inband-Tönen für den-Befehl.                                                            |
| [**linesetmediacontrol**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Aktiviert und deaktiviert Steuerungs Aktionen für den Mediendaten Strom, der der angegebenen Zeile, Adresse oder dem angegebenen-Befehl zugeordnet ist.             |



 



| TAPI 3. x-Schnittstellen oder-Methoden                               | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itlegacycallmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Unterstützt Legacy Anwendungen, die direkt mit einem Gerät kommunizieren müssen.                                                                                                                             |
| [**Itlegacywavesupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Ermöglicht es einer Anwendung zu ermitteln, ob ein Terminal, das von einem Legacy-TSP (Pre-TAPI 3) erstellt wurde, mithilfe der Wave-API gesteuert werden kann.                                                                        |
| [**Itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Ermöglicht einer Anwendung das Abrufen von Informationen zu einem Stream. , wenn der Stream gestartet, angehalten oder beendet werden soll. So können Sie Terminals in einem Stream auswählen oder die Auswahl deaktivieren und zum Abrufen einer Liste der im Stream ausgewählten Terminals. |
| [**Itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Ermöglicht einer Anwendung das aufzählen, erstellen oder Entfernen von Mediendaten strömen.                                                                                                                                   |



 

 

 
