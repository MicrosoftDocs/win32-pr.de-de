---
description: Schnittstellen für DirectShow-Bearbeitungsdienste
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Schnittstellen für DirectShow-Bearbeitungsdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e913ec6bf17a11a4b772d288b9404113cd6bdc70bf441ed20dcbc69a086f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397591"
---
# <a name="interfaces-for-directshow-editing-services"></a>Schnittstellen für DirectShow-Bearbeitungsdienste

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Dieser Abschnitt enthält Referenzthemen für die [DirectShow Editing Services-Schnittstellen](directshow-editing-services.md) (DES).



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Stellt eine Rückrufmethode für die Fehlerprotokollierung bereit.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Legt ein Fehlerprotokoll fest oder ruft es ab.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Stellt Methoden zum Bearbeiten der Zeitachse bereit.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Fügt virtuelle Spuren für eine Komposition ein oder ruft sie ab.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Stellt Methoden zum Bearbeiten von Zeitachseneffekten bereit.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Stellt Methoden zum Hinzufügen von Effekten zu einem Zeitachsenobjekt bereit.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Legt Eigenschaften für Gruppen fest und ruft sie ab.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Stellt Methoden zum Bearbeiten von Zeitachsenobjekten bereit.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Teilt ein Zeitachsenobjekt auf.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quellobjekte bereit.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Stellt Methoden zum Bearbeiten von Verfolgungsobjekten bereit.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Stellt Methoden zum Bearbeiten von Übergangsobjekten bereit.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Fügt Übergänge zu einem Objekt hinzu.                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Stellt Methoden zum Arbeiten mit virtuellen Spuren bereit.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Legt Eigenschaften für den [Alphasetter-Effekt fest.](alpha-setter-effect.md)                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Legt Eigenschaften für den [Compositorübergang](compositor-transition.md) fest.                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Legt Eigenschaften für den [SMPTE-Zurücksetzungsübergang](smpte-wipe-transition.md) fest.                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Legt Eigenschaften für den [Schlüsselübergang](key-transition.md) fest.                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | Wird nicht unterstützt.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | Wird nicht unterstützt.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Ruft Informationen zu einer Mediendatei ab, z. B. die Anzahl der Datenströme und den Typ, die Dauer und die Bildfrequenz jedes Streams. |
| [**IMediaLocator**](imedialocator.md)                     | Stellt Methoden zum Überprüfen von Dateinamen bereit.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Legt Eigenschaften für einen Effekt oder Übergang fest.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Rendert ein DES-Projekt, indem ein Filterdiagramm aus einer Zeitachse erstellt wird.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Ermöglicht der Anwendung, den vom DES verwendeten Standardfilter für die Größenänderung von Videos zu ersetzen.                                              |
| [**IResize**](iresize.md)                                 | Muss von einem benutzerdefinierten Videoänderungsfilter unterstützt werden.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Ruft einzelne Medienbeispiele ab, während sie sich durch das Filterdiagramm bewegen.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Rückrufschnittstelle für die [**ISampleGrabber-Schnittstelle.**](isamplegrabber.md)                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Stellt Methoden bereit, die die intelligente Neukomprimierung unterstützen.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Speichert und lädt DES-Projektdateien in Extensible Markup Language (XML).                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[C++-Referenz zu DirectShow Editing Services](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



