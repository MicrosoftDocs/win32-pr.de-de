---
description: Schnittstellen für DirectShow-Bearbeitungs Dienste
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Schnittstellen für DirectShow-Bearbeitungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba286a340693407287ed370ed401ac6b039593c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747112"
---
# <a name="interfaces-for-directshow-editing-services"></a>Schnittstellen für DirectShow-Bearbeitungs Dienste

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Dieser Abschnitt enthält Referenz Themen für die Schnittstellen der [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (des).



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Iamerrorlog**](iamerrorlog.md)                         | Stellt eine Rückruf Methode für die Fehler Protokollierung bereit.                                                                                  |
| [**Iameinterrorlog**](iamseterrorlog.md)                   | Legt ein Fehlerprotokoll fest oder ruft es ab.                                                                                                |
| [**Iamtimeline**](iamtimeline.md)                         | Stellt Methoden zum Bearbeiten der Zeitachse bereit.                                                                                |
| [**Iamtimelinecomp**](iamtimelinecomp.md)                 | Fügt virtuelle Spuren in einer Komposition ein oder ruft Sie ab.                                                                          |
| [**Iamtimelineeffect**](iamtimelineeffect.md)             | Stellt Methoden zum Bearbeiten von Zeitachsen Effekten bereit.                                                                            |
| [**Iamtimelineeffectable**](iamtimelineeffectable.md)     | Stellt Methoden zum Hinzufügen von Effekten zu einem Zeitachsen Objekt bereit.                                                                      |
| [**Iamtimelinegroup**](iamtimelinegroup.md)               | Legt Eigenschaften für Gruppen fest und ruft Sie ab.                                                                                       |
| [**Iamtimelineobj**](iamtimelineobj.md)                   | Stellt Methoden zum Bearbeiten von Zeitachsen Objekten bereit.                                                                            |
| [**Iamtimelinesplicustom**](iamtimelinesplittable.md)     | Teilt ein Zeitachsen Objekt.                                                                                                      |
| [**Iamtimelinesrc**](iamtimelinesrc.md)                   | Stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quell Objekte bereit.                                                    |
| [**Iamtimelinetrack**](iamtimelinetrack.md)               | Stellt Methoden zum Bearbeiten von Track-Objekten bereit.                                                                               |
| [**Iamtimelinetrans**](iamtimelinetrans.md)               | Stellt Methoden zum Bearbeiten von Übergangs Objekten bereit.                                                                          |
| [**Iamtimelinetransable**](iamtimelinetransable.md)       | Fügt einem-Objekt Übergänge hinzu.                                                                                                 |
| [**Iamtimelinevirtualtrack**](iamtimelinevirtualtrack.md) | Stellt Methoden zum Arbeiten mit virtuellen Spuren bereit.                                                                              |
| [**Idxtalphasetter**](idxtalphasetter.md)                 | Legt Eigenschaften für den [Alpha Setter](alpha-setter-effect.md) -Effekt fest.                                                         |
| [**Idxtcompositor**](idxtcompositor.md)                   | Legt Eigenschaften für den [compositorübergang](compositor-transition.md) fest.                                                     |
| [**Idxtjpeg**](idxtjpeg.md)                               | Legt die Eigenschaften des [SMPTE](smpte-wipe-transition.md) -zurücksetzen-Übergangs fest.                                                     |
| [**Idxtkey**](idxtkey.md)                                 | Legt Eigenschaften für den [Schlüssel](key-transition.md) Übergang fest.                                                                   |
| [**Ifindcompressorcb**](ifindcompressorcb.md)             | Wird nicht unterstützt.                                                                                                                 |
| [**Igrf Cache**](igrfcache.md)                             | Wird nicht unterstützt.                                                                                                                 |
| [**Imediadet**](imediadet.md)                             | Ruft Informationen zu einer Mediendatei ab, z. b. die Anzahl der Streams und Typ, Dauer und Framerate der einzelnen Datenströme. |
| [**Imedialocator**](imedialocator.md)                     | Stellt Methoden zum Validieren von Dateinamen bereit.                                                                                    |
| [**Ipropertysetter**](ipropertysetter.md)                 | Legt die Eigenschaften eines Effekts oder Übergangs fest.                                                                                    |
| [**"Unenderengine"**](irenderengine.md)                     | Rendert ein des-Projekts durch Erstellen eines Filter Diagramms aus einer Zeitachse.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Ermöglicht es der Anwendung, den von des verwendeten Standardfilter für die Videogröße zu ersetzen.                                              |
| [**Iresize**](iresize.md)                                 | Muss von jedem benutzerdefinierten Filter zum Ändern der Größe von Videos unterstützt werden.                                                                          |
| [**Isamplegrabber**](isamplegrabber.md)                   | Ruft einzelne Medien Beispiele beim Durchlaufen des Filter Diagramms ab.                                                      |
| [**Isamplegrabbercb**](isamplegrabbercb.md)               | Rückruf Schnittstelle für die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle.                                                 |
| [**Ismartrenderengine**](ismartrenderengine.md)           | Stellt Methoden bereit, die intelligente Neukomprimierung unterstützen.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Speichert und lädt des-Projektdateien in Extensible Markup Language (XML).                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Bearbeitungs Dienste C++ Referenz](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



