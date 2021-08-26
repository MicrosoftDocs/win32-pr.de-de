---
title: Anwendungswiederherstellung und Neustart
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um eine Anwendung, die heruntergefahren wurde, automatisch neu zu starten, um ein Update abzuschließen. Speichern Sie Daten, und konfigurieren Sie die Anwendungswiederherstellung, bevor Sie Programme beenden.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- Zuverlässigkeit
- Software-Zuverlässigkeit
- Anwendungswiederherstellung
- Neustart der Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31d6c8ef342b9e1781297d547358317a90d515002e6ef3e529b8d7a0c50aa09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024600"
---
# <a name="application-recovery-and-restart"></a>Anwendungswiederherstellung und Neustart

## <a name="purpose"></a>Zweck

Eine Anwendung kann Application Recovery and Restart (ARR) verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird auch neu gestartet, falls dies angefordert wird.

Eine Anwendung kann auch neu gestartet werden, wenn ein Installationsprogramm eine Komponente der Anwendung aktualisiert oder wenn der Computer als Ergebnis eines Updates neu gestartet werden muss. Beachten Sie, dass sowohl die Anwendung als auch das Installationsprogramm entsprechend erstellt werden müssen, um den automatischen Anwendungsneustart zu unterstützen, nachdem ein Installationsprogramm eine Anwendung aktualisiert hat. Weitere Informationen finden Sie unter [Registrieren für den Anwendungsneustart.](registering-for-application-restart.md)

## <a name="developer-audience"></a>Entwicklergruppe

ARR ist für C- und C++-Entwickler konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

ARR ist ab dem Betriebssystem Windows Vista verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Verwenden von Anwendungswiederherstellung und Neustart](using-application-recovery-and-restart.md)<br/>         | Anleitung zum Registrieren für die Wiederherstellung und den Neustart.<br/> |
| [Anwendungswiederherstellungs- und Neustartreferenz](application-recovery-and-restart-reference.md)<br/> | Referenzinformationen für die ARR-API. <br/>                    |



 

 

 





