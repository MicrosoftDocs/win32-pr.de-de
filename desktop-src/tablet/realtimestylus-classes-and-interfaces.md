---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echtzeit-Stift verwendet werden.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: RealTimeStylus-Klassen und -Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd842219a23accc076ff7fdc8564ccb3ce0c472cb7e26ab036f1048456461f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589950"
---
# <a name="realtimestylus-classes-and-interfaces"></a>RealTimeStylus-Klassen und -Schnittstellen

Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echtzeit-Stift verwendet werden.

> [!Note]  
> Die Stylusklassen und Schnittstellen in Echtzeit sind nicht automation-kompatibel.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Klasse                                                      | Beschreibung                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus-Klasse**](realtimestylus-class.md)       | Implementiert die [**IRealTimeStylus-Schnittstelle.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)<br/>                 |
| [**DynamicRenderer-Klasse**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementiert die [**IDynamicRenderer-Schnittstelle.**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)<br/>     |
| [**GestureRecognizer-Klasse**](gesturerecognizer-class.md) | Implementiert die [**IGestureRecognizer-Schnittstelle.**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)<br/> |
| [**StrokeBuilder-Klasse**](strokebuilder-class.md)         | Implementiert die [**Schnittstelle IStrokeBuilder-Schnittstelle.**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)<br/>         |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDynamicRenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Macht Methoden verfügbar, mit denen Sie die Anzeige von Stiftdaten in Echtzeit steuern können, während die Daten vom [**RealTimeStylus Class-Objekt**](realtimestylus-class.md) verarbeitet werden.<br/> |
| [**IGestureRecognizer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Macht Methoden verfügbar, mit denen Sie auf Ereignisse reagieren können, indem Sie Stiftgesten erkennen und der Eingabewarteschlange Daten hinzufügen.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Verarbeitet die Stiftpaketdaten aus einem Digitizer in Echtzeit.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Erweitert die IRealTimeStylus-Schnittstelle.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Erweitert die IRealTimeStylus-Schnittstelle.<br/>                                                                                                                                           |
| [**IRealTimeStylusSynchronization-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Synchronisiert den Zugriff auf das [**RealTimeStylus-Klassenobjekt.**](realtimestylus-class.md)<br/>                                                                                          |
| [**IStrokeBuilder-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Macht Methoden verfügbar, mit denen Sie Striche programmgesteuert erstellen können.<br/>                                                                                                              |
| [**IStylusPlugin-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Macht Methoden verfügbar, mit denen Sie Benachrichtigungen über Ereignisse empfangen und basierend auf diesen Ereignissen eine benutzerdefinierte Verarbeitung durchführen können.<br/>                                                          |
| [**Istylusasyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Stellt ein asynchrones Plug-In dar, das der asynchronen Plug-In-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.<br/>                                |
| [**Istylussyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Stellt ein synchrones Plug-In dar, das der synchronen Plug-In-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.<br/>                                   |



 

## <a name="return-values"></a>Rückgabewerte

Methoden in der COM-Bibliothek geben Werte von **HRESULT** zurück. Sofern nicht anders angegeben, werden die Bedeutungen der **HRESULT-Werte** in der folgenden Tabelle beschrieben.



| HRESULT-Wert                                   | Beschreibung                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Erfolg.<br/>                                                                      |
| E \_ POINTER<br/>                           | Mindestens ein Zeiger (für eine Eingabe oder einen Ausgabeparameter) ist ungültig.<br/> |
| E \_ INVALIDARG<br/>                        | Member hat versucht, ein ungültiges Argument zu übergeben.<br/>                              |
| E \_ INK \_ EXCEPTION<br/>                    | Ausnahme.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | Das System kann keinen Arbeitsspeicher belegen, um den Vorgang abzuschließen.<br/>                      |
| E \_ FAIL<br/>                              | Es ist ein nicht angegebener Fehler aufgetreten.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Member hat versucht, einen ungültigen Vorgang zu verwenden.<br/>                                 |
| UNGÜLTIGER TPC \_ \_ \_ E-MODUS<br/>                | Member hat versucht, einen ungültigen Modus zu verwenden.<br/>                                      |
| TPC \_ E \_ INVALID \_ CONFIGURATION<br/>       | Der Member hat versucht, eine ungültige Konfiguration zu verwenden.<br/>                             |
| TPC \_ E \_ INVALID \_ PACKET \_ DESCRIPTION<br/> | Member hat versucht, eine ungültige Paketbeschreibung zu verwenden.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RealTimeStylus-Referenz](realtimestylus-reference.md)
</dt> </dl>

 

 
