---
title: Verwenden von IMAPI
description: In den folgenden Themen wird die Verwendung der Image-Mastering-API veranschaulicht.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856948"
---
# <a name="using-imapi"></a>Verwenden von IMAPI

In den folgenden Themen wird die Verwendung der Image-Mastering-API veranschaulicht.

## <a name="usage-scenarios"></a>Verwendungsszenarien

In der folgenden Dokumentation finden Sie ausführliche Anleitungen für gängige IMAPI-Szenarios.



| Szenario                                                                                                         | BESCHREIBUNG                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Überprüfen der Laufwerk Unterstützung](checking-drive-support.md)                                                             | Veranschaulicht das Erkennen der Unterstützung für ein Medienlaufwerk.<br/>                                                                                                   |
| [Überprüfen der Medien Unterstützung](checking-media-support.md)                                                             | Veranschaulicht das Erkennen der Unterstützung für Medien.<br/>                                                                                                           |
| [Brennen eines Festplatten Bilds](burning-a-disc.md)                                                                       | Veranschaulicht das Mastering (Brennen eines Datenträgers) mithilfe von IMAPI.<br/>                                                                                                       |
| [Hinzufügen eines Start Abbilds](adding-a-boot-image.md)                                                                   | Basiert auf dem Beispiel zum [Brennen eines Festplatten Bilds](burning-a-disc.md) durch Hinzufügen von Code, um ein startbares Image in den Startbereich der Festplatte einzubeziehen.<br/>               |
| [Erstellen einer Multi-Session-CD](creating-a-multisession-disc.md)                                                 | Veranschaulicht die Erstellung einer mehr sitzungsdatenträger mithilfe von IMAPI.<br/>                                                                                              |
| [Überwachen des Fortschritts mit Ereignissen](monitoring-progress-with-events.md)                                           | Veranschaulicht die Verwendung spezifischer Schnittstellen, um die Implementierung eines Ereignis Handlers zuzulassen, damit Statusinformationen empfangen werden können. <br/>        |
| [Verhindern der Abmeldung oder aussetzen während eines Burn-Vorgangs](preventing-logoff-or-suspend-during-a-burn.md)                     | Enthält Informationen über Aspekte der Anwendungsentwicklung in Bezug auf Szenarien, in denen der Benutzer "Abmeldung" und "Suspend" in Windows berücksichtigt werden.<br/> |
| [Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte](providing-user-permissions-for-media-burning-devices.md) | Erläutert den Prozess, der erforderlich ist, um sicherzustellen, dass ein Benutzer über die erforderlichen Berechtigungen zum Verwenden von Medien brennen auf Windows XP und Windows Server 2003 verfügt.<br/>             |



 

## <a name="application-compatibility"></a>Anwendungskompatibilität

Die folgende Dokumentation enthält wichtige Informationen, die beim Entwickeln einer Anwendung, die IMAPI verwendet, berücksichtigt werden müssen.



| Leitfaden                                                   | Beschreibung                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Layout von IMAPI-Multisession](imapi-multisession-layout.md) | Erläutert das Festplattenlayout, das von IMAPI zum Implementieren von mehreren Sitzungen verwendet wird. Diese Informationen werden verwendet, um die Interoperabilität zwischen IMAPI und anderer brennender Software zu gewährleisten und das Erstellen von IMAPI-kompatiblen Festplatten Abbildern mit mehreren Sitzungen zu ermöglichen.<br/> |



 

 

 





