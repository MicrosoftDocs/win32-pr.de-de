---
title: MediaRenderer-Klasse
description: Implementiert die imediarenderer-Schnittstelle, die ein DLNA Digital Media-Renderer-Gerät (DMR) darstellt.
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- Media Streaming-API der MediaRenderer-Klasse
- Media Streaming-API der MediaRenderer-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d14cdea89535fc680874905a9fb2b3358595baab
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516739"
---
# <a name="mediarenderer-class"></a>MediaRenderer-Klasse

Implementiert die [**imediarenderer**](imediarenderer.md) -Schnittstelle, die ein DLNA Digital Media-Renderer-Gerät (DMR) darstellt.

**MediaRenderer** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MediaRenderer** -Klasse verfügt über diese Methoden.



| Methode                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_renderingparametersupdate hinzufügen**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Registriert einen Ereignishandler für das [**renderingparametersupdate**](renderingparametersupdate.md) -Ereignis.<br/>                                                                                                                                                                                                                                                       |
| [**\_transportparametersupdate hinzufügen**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Registriert einen Ereignishandler für das [**transportparametersupdate**](transportparametersupdate.md) -Ereignis.<br/>                                                                                                                                                                                                                                                       |
| [**Getmuteasync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Fragt den DMR asynchron ab, um zu bestimmen, ob Audiodaten derzeit stumm oder unstumm geschaltet werden.<br/>                                                                                                                                                                                                                                                                            |
| [**Getpositioninformationasync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Fragt den DMR asynchron ab, um Positionsinformationen abzurufen.<br/>                                                                                                                                                                                                                                                                                               |
| [**Gettransportinformationasync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Fragt den DMR asynchron ab, um Transportinformationen abzurufen.<br/>                                                                                                                                                                                                                                                                                              |
| [**Getvolumeasync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Fragt den DMR asynchron nach der aktuellen audiovolumeebene ab.<br/>                                                                                                                                                                                                                                                                                             |
| [**Pauchasync**](mediarenderer-pauseasync.md)                                               | Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.<br/>                                                                                                                                                                                                                                                                                         |
| [**Playasync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Weist den DMR asynchron an, den Inhalt wiederzugeben, der durch Aufrufen der [**setsourcefromuriasync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))-, [**setsourcefromstreamasync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))-oder [**setsourcefrommediasourceasync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) -Methode angegeben wurde.<br/>                       |
| [**Playatspeedasync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Weist den DMR asynchron an, den Inhalt wiederzugeben, der durch Aufrufen der [**setsourcefromuriasync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))-, [**setsourcefromstreamasync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))-oder [**setsourcefrommediasourceasync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) -Methode mit der angegebenen Rate angegeben wurde.<br/> |
| [**\_renderingparametersupdate entfernen**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Hebt die Registrierung eines Ereignis Handlers für das [**renderingparametersupdate**](renderingparametersupdate.md) -Ereignis auf.<br/>                                                                                                                                                                                                                                                     |
| [**\_transportparametersupdate entfernen**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Hebt die Registrierung eines Ereignis Handlers für das [**transportparametersupdate**](transportparametersupdate.md) -Ereignis auf.<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Weist den DMR asynchron an, einen bestimmten Zeit Offset zu suchen.<br/>                                                                                                                                                                                                                                                                                          |
| [**Setmuteasync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Weist den DMR asynchron an, das Audiogerät stumm zu schalten oder zu entstumm schalten.<br/>                                                                                                                                                                                                                                                                                           |
| [**Setnextsourcefrommediasourceasync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Weist den DMR asynchron an, den angegebenen Inhalt für die Wiedergabe vorzubereiten, sobald die Wiedergabe des aktuellen Inhalts beendet ist.<br/>                                                                                                                                                                                                                                   |
| [**Setnextsourcefromstreamasync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Weist den DMR asynchron an, den angegebenen Mediendaten Strom für die Wiedergabe vorzubereiten, sobald die Wiedergabe des aktuellen Inhalts beendet ist.<br/>                                                                                                                                                                                                                              |
| [**Setnextsourcefromuriasync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Weist den DMR asynchron an, den durch den angegebenen URI identifizierten Inhalt für die Wiedergabe vorzubereiten, sobald die Wiedergabe des aktuellen Inhalts beendet ist.<br/>                                                                                                                                                                                                             |
| [**Setsourcefrommediasourceasync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Weist den DMR asynchron an, den angegebenen Inhalt für die Wiedergabe vorzubereiten.<br/>                                                                                                                                                                                                                                                                                 |
| [**Setsourcefromstreamasync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Weist den DMR asynchron an, den angegebenen Mediendaten Strom für die Wiedergabe vorzubereiten, sobald die Wiedergabe des aktuellen Inhalts beendet ist.<br/>                                                                                                                                                                                                                              |
| [**Setsourcefromuriasync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Weist den DMR asynchron an, den Inhalt vorzubereiten, der durch den angegebenen URI für die Wiedergabe festgelegt wurde.<br/>                                                                                                                                                                                                                                                           |
| [**Setvolumeasync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Legt die audiovolumeebene für den DMR asynchron auf den angegebenen Wert fest.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Eigenschaften

Die **MediaRenderer** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | BESCHREIBUNG                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**Aktions Informationen**](mediarenderer-actioninformation.md)<br/> | Schreibgeschützt<br/> | Ruft Informationen darüber ab, welche Methoden derzeit für den DMR aufgerufen werden können.<br/>        |
| [**Isaudiosupported**](mediarenderer-isaudiosupported.md)<br/>   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob der DMR Audioinhalt abspielen kann.<br/> |
| [**Isimagesupported**](mediarenderer-isimagesupported.md)<br/>   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob der DMR Bilder anzeigen kann.<br/>     |
| [**Isvideosupported**](mediarenderer-isvideosupported.md)<br/>   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob der DMR Videoinhalte abspielen kann.<br/> |



 

 

