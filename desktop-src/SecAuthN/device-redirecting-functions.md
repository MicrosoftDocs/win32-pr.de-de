---
description: Die Funktionen zum Umleiten von Geräten leiten Standard-MS-DOS-Geräte, Laufwerk Buchstaben und LPT-Ports um. Auf diese Weise können Anwendungen, die auf dem System ausgeführt werden, die Geräte verwenden und auf das Netzwerk vollständig transparent zugreifen.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214410"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting Funktionen

Die Funktionen zum Umleiten von Geräten leiten Standard-MS-DOS-Geräte, Laufwerk Buchstaben und LPT-Ports um. Auf diese Weise können Anwendungen, die auf dem System ausgeführt werden, die Geräte verwenden und auf das Netzwerk vollständig transparent zugreifen.



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Npaddconnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Leitet ein lokales Gerät an eine Netzwerkressource um und stellt eine Verbindung her.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Führt dieselbe Aktion wie [**npaddconnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)aus, ermöglicht jedoch dem Benutzer anzugeben, welches Fenster die Besitzer von Dialogfeldern sein soll und wie die Verbindung hergestellt werden soll.<br/> |
| [**Npcancelconnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Unterbricht eine Netzwerkverbindung. Die Änderungen werden gespeichert, wenn ein Gerät getrennt wird, es sei denn, es handelt sich um eine nicht beliebige Verbindung.<br/>                                                    |
| [**Npgetconnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Gibt Informationen über eine Verbindung zurück.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Gibt Informationen zu einer Verbindung zurück, auch wenn die Verbindung zurzeit getrennt ist.<br/>                                                                                                |
| [**Npgetconnectionperformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Gibt Leistungsinformationen zu einer Verbindung zurück.<br/>                                                                                                                                      |
| [**Npgetuniversalname**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Gibt den Remote-oder lokalen universellen Namen in dem während des Funktions Aufrufes angegebenen Format zurück.<br/>                                                                                            |



 

 

 




