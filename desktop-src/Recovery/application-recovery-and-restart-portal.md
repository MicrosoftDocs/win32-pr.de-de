---
title: Anwendungswiederherstellung und Neustart
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um eine herunter gefahrene Anwendung automatisch neu zu starten, um ein Update abzuschließen. Speichern von Daten und Konfigurieren der Anwendungs Wiederherstellung vor dem Beenden der Programme.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- Zuverlässigkeit
- Software Zuverlässigkeit
- Anwendungs Wiederherstellung
- Anwendungs Neustart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856803"
---
# <a name="application-recovery-and-restart"></a>Anwendungswiederherstellung und Neustart

## <a name="purpose"></a>Zweck

Eine Anwendung kann die Anwendungs Wiederherstellung und den Neustart (arr) verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird, oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird bei Bedarf ebenfalls neu gestartet.

Eine Anwendung kann auch neu gestartet werden, wenn ein Installer eine Komponente der Anwendung aktualisiert oder wenn der Computer aufgrund eines Updates neu gestartet werden muss. Beachten Sie, dass die Anwendung und das Installationsprogramm entsprechend erstellt werden müssen, um den automatischen Neustart der Anwendung zu unterstützen, nachdem ein Installer eine Anwendung aktualisiert hat. Weitere Informationen finden Sie unter [registrieren für den Neustart der Anwendung](registering-for-application-restart.md).

## <a name="developer-audience"></a>Entwicklergruppe

ARR ist für C-und C++-Entwickler konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

ARR ist ab dem Betriebssystem Windows Vista verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Verwenden von Anwendungs Wiederherstellung und Neustart](using-application-recovery-and-restart.md)<br/>         | Handbuch für die Registrierung für die Wiederherstellung und den Neustart.<br/> |
| [Anwendungs Wiederherstellung und Neustart Referenz](application-recovery-and-restart-reference.md)<br/> | Referenzinformationen für die ARR-API. <br/>                    |



 

 

 





