---
title: Verwenden von IMAPI
description: In den folgenden Themen wird die Verwendung der Imagemastering-API veranschaulicht.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf19d619f6ed5ab9a2d6b0deb1ca6a42b71a0b0941a96f54cccfa87c14b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092430"
---
# <a name="using-imapi"></a>Verwenden von IMAPI

In den folgenden Themen wird die Verwendung der Imagemastering-API veranschaulicht.

## <a name="usage-scenarios"></a>Verwendungsszenarien

Die folgende Dokumentation enthält ausführliche Anleitungen für gängige IMAPI-Szenarien.



| Szenario                                                                                                         | BESCHREIBUNG                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Überprüfen der Laufwerkunterstützung](checking-drive-support.md)                                                             | Veranschaulicht die Erkennung der Unterstützung für ein Medienlaufwerk.<br/>                                                                                                   |
| [Überprüfen der Medienunterstützung](checking-media-support.md)                                                             | Veranschaulicht die Erkennung der Unterstützung für Medien.<br/>                                                                                                           |
| [Verwerfen eines Datenträgerbilds](burning-a-disc.md)                                                                       | Veranschaulicht das Mastering (Aufschlüsseln eines Datenträgers) mithilfe der IMAPI.<br/>                                                                                                       |
| [Hinzufügen eines Startimages](adding-a-boot-image.md)                                                                   | Baut auf dem Beispiel [Zum Erstellen eines Datenträgerimages](burning-a-disc.md) auf, indem Code hinzugefügt wird, um ein startbares Image in den Startabschnitt des Datenträgers einzuschließen.<br/>               |
| [Erstellen eines Multisession-Datenträgers](creating-a-multisession-disc.md)                                                 | Veranschaulicht die Erstellung eines Multisession-Datenträgers mithilfe der IMAPI.<br/>                                                                                              |
| [Überwachen des Fortschritts mit Ereignissen](monitoring-progress-with-events.md)                                           | Veranschaulicht die Verwendung bestimmter Schnittstellen, um die Implementierung eines Ereignishandlers zu ermöglichen, sodass Statusinformationen empfangen werden können. <br/>        |
| [Verhindern des Abmeldens oder Anhaltens während eines Brandes](preventing-logoff-or-suspend-during-a-burn.md)                     | Enthält Informationen zu Überlegungen zur Anwendungsentwicklung, die in Bezug auf Szenarien mit "Logoff" und "Suspend" in Windows zu berücksichtigen sind.<br/> |
| [Bereitstellen von Benutzerberechtigungen für Mediengeräte](providing-user-permissions-for-media-burning-devices.md) | Beschreibt den Prozess, der erforderlich ist, um sicherzustellen, dass ein Benutzer über ausreichende Berechtigungen zum Verwenden von Mediengeräten auf Windows XP und Windows Server 2003 verfügt.<br/>             |



 

## <a name="application-compatibility"></a>Anwendungskompatibilität

Die folgende Dokumentation enthält wichtige Informationen, die beim Entwickeln einer Anwendung, die IMAPI verwendet, zu berücksichtigen sind.



| Leitfaden                                                   | Beschreibung                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IMAPI-Multisessionlayout](imapi-multisession-layout.md) | Beschreibt das Datenträgerlayout, das die IMAPI zum Implementieren von Multisession verwendet. Diese Informationen werden verwendet, um die Interoperabilität zwischen IMAPI und anderer Software sicherzustellen und die Erstellung von IMAPI-kompatiblen Multisession-Datenträgerimages zu ermöglichen.<br/> |



 

 

 





