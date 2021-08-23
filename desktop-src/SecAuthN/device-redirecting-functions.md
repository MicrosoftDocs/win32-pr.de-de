---
description: Die Geräteumleitungsfunktionen leiten MS-DOS-Standardgeräte, Laufwerkbuchstaben und LPT-Ports um. Dies ermöglicht anwendungen, die auf dem System ausgeführt werden, die Geräte zu verwenden und auf völlig transparente Weise auf das Netzwerk zuzugreifen.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4929052ed2691d6264791cac431e59faaacdb92f7f96bb610d99fdd4ded471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008448"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting Functions

Die Geräteumleitungsfunktionen leiten MS-DOS-Standardgeräte, Laufwerkbuchstaben und LPT-Ports um. Dies ermöglicht anwendungen, die auf dem System ausgeführt werden, die Geräte zu verwenden und auf völlig transparente Weise auf das Netzwerk zuzugreifen.



| Funktion                                                         | Beschreibung                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Leitet ein lokales Gerät um oder verbindet es mit einer Netzwerkressource.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Führt die gleiche Aktion wie [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)aus, ermöglicht dem Benutzer jedoch, anzugeben, welches Fenster die Dialogfelder besitzen soll und wie die Verbindung hergestellt werden soll.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Unterbricht eine Netzwerkverbindung. Die Änderungen werden gespeichert, wenn ein Gerät getrennt wird, es sei denn, die Verbindung ist eine gerätelose Verbindung.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Gibt Informationen zu einer Verbindung zurück.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Gibt Informationen zu einer Verbindung zurück, auch wenn die Verbindung derzeit getrennt ist.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Gibt Leistungsinformationen zu einer Verbindung zurück.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Gibt den remoten oder lokalen universellen Namen in dem Format zurück, das während des Funktionsaufrufs angegeben wurde.<br/>                                                                                            |



 

 

 




