---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echt Zeit Tablettstift verwendet werden.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: RealTimeStylus-Klassen und-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866132"
---
# <a name="realtimestylus-classes-and-interfaces"></a>RealTimeStylus-Klassen und-Schnittstellen

Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echt Zeit Tablettstift verwendet werden.

> [!Note]  
> Die Klassen und Schnittstellen für echt Zeit Stile sind nicht Automatisierungs konform.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Klasse                                                      | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus-Klasse**](realtimestylus-class.md)       | Implementiert die [**irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -Schnittstelle.<br/>                 |
| [**DynamicRenderer-Klasse**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementiert die [**Schnittstelle der idynamicrenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .<br/>     |
| [**GestureRecognizer-Klasse**](gesturerecognizer-class.md) | Implementiert die [**igesturerecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) -Schnittstelle.<br/> |
| [**Strokebuilder-Klasse**](strokebuilder-class.md)         | Implementiert die [**istrokebuilder-Schnittstellen**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) Schnittstelle.<br/>         |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Idynamicrenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Macht Methoden verfügbar, mit denen Sie die Anzeige von Tablettstiftdaten in Echtzeit steuern können, wenn die Daten vom [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt verarbeitet werden.<br/> |
| [**Igesturerecognizer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Macht Methoden verfügbar, mit denen Sie auf Ereignisse reagieren können, indem Sie Stift Bewegungen erkennen und Daten zur Eingabe Warteschlange hinzufügen.<br/>                                                  |
| [**Irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Verarbeitet die tablettstiftpaketdaten von einem Digitalisierer in Echtzeit.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Erweitert die irealtimestylus-Schnittstelle.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Erweitert die irealtimestylus-Schnittstelle.<br/>                                                                                                                                           |
| [**Irealtimestylussynchronization-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Synchronisiert den Zugriff auf das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt.<br/>                                                                                          |
| [**Istrokebuilder-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Macht Methoden verfügbar, die es Ihnen ermöglichen, Striche Programm gesteuert zu erstellen.<br/>                                                                                                              |
| [**Istylusplugin-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Macht Methoden verfügbar, mit denen Sie Benachrichtigungen zu Ereignissen empfangen und auf der Grundlage dieser Ereignisse eine benutzerdefinierte Verarbeitung durchführen können.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Stellt ein asynchrones Plug-in dar, das der asynchronen Plug-in-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Stellt ein synchrones Plug-in dar, das der synchronen Plug-in-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.<br/>                                   |



 

## <a name="return-values"></a>Rückgabewerte

Methoden in der com-Bibliothek geben Werte von **HRESULT** zurück. Sofern nicht anders angegeben, werden die Bedeutungen der **HRESULT** -Werte in der folgenden Tabelle beschrieben.



| HRESULT-Wert                                   | BESCHREIBUNG                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Erfolg.<br/>                                                                      |
| E- \_ Zeiger<br/>                           | Mindestens ein Zeiger (entweder für einen Eingabe-oder einen Output-Parameter) ist ungültig.<br/> |
| E \_ invalidArg<br/>                        | Der Member hat versucht, ein ungültiges Argument zu übergeben.<br/>                              |
| E- \_ Ink- \_ Ausnahme<br/>                    | Ausnahme.<br/>                                                           |
| E \_ outo-Memory<br/>                       | Das System kann keinen Arbeitsspeicher zuweisen, um den Vorgang abzuschließen.<br/>                      |
| E \_ fehlschlagen<br/>                              | Ein nicht spezifizierter Fehler ist aufgetreten.<br/>                                                 |
| E \_ InvalidOperation<br/>                  | Der Member hat versucht, einen ungültigen Vorgang zu verwenden.<br/>                                 |
| TPC \_ E \_ ungültiger \_ Modus<br/>                | Der Member hat versucht, einen ungültigen Modus zu verwenden.<br/>                                      |
| TPC \_ E \_ - \_ Konfiguration ungültig<br/>       | Der Member hat versucht, eine ungültige Konfiguration zu verwenden.<br/>                             |
| TPC \_ E \_ ungültige \_ Paket \_ Beschreibung<br/> | Der Member hat versucht, eine ungültige Paketbeschreibung zu verwenden.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RealTimeStylus-Referenz](realtimestylus-reference.md)
</dt> </dl>

 

 
