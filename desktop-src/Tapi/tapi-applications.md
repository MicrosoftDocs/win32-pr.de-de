---
description: Das folgende Material enthält Richtlinien für die Verwendung von TAPI zum Schreiben von Anwendungen für die Endbenutzer-oder Serverkommunikation. Diese Informationen sind auch für Dienstanbieter Programmierer äußerst relevant.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: TAPI-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369804"
---
# <a name="tapi-applications"></a>TAPI-Anwendungen

Das folgende Material enthält Richtlinien für die Verwendung von TAPI zum Schreiben von Anwendungen für die Endbenutzer-oder Serverkommunikation. Diese Informationen sind auch für Dienstanbieter Programmierer äußerst relevant.

Die erste Entscheidung, die ein Programmierer bei der Verwendung von TAPI treffen muss, ist die erforderliche Dienst Ebene. Wenn eine Anwendung z. b. eine Menü Auswahl erfordert, die eine Telefonnummer wählen kann, ist wahrscheinlich keine vollständige TAPI-Anwendung erforderlich. Unterstützte Telefonieoptionen können diese Option schnell und einfach aktivieren. Weitere Informationen zum Unterschied zwischen vollständigen TAPI-Anwendungen und der unterstützten Telefonie finden Sie unter [TAPI-Dienst Ebenen](tapi-levels-of-service.md) .

Die zweite wichtige Entscheidung ist, ob TAPI 2. x, die C-basierte API oder TAPI 3. x, die auf com basiert, verwendet werden soll. Eine Erörterung wichtiger Aspekte bei der Entscheidung, welche verwendet werden soll, finden Sie unter [TAPI 3. x vs. TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) .

Im folgenden Diagramm werden die grundlegenden Bausteine einer vollständigen TAPI-Anwendung veranschaulicht. TAPI 2. x und TAPI 3. x werden in diesen Abschnitten behandelt. Material, das sehr spezifisch ist, wird in den Übersichts Abschnitten für TAPI 2. x oder TAPI 3. x behandelt.

![Bausteine einer TAPI-Anwendung](images/tapior3.png)

Die folgenden Links stellen Inhalt bereit, der den Abbildungen in der obigen Abbildung entspricht:

| Re | Dokumentation                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [TAPI-Initialisierung](tapi-initialization.md)                                   |
| 2      | [Sitzungssteuerung](session-control.md)                                           |
| 3      | [Gerätesteuerung](device-control.md)                                             |
| 4      | [Mediensteuer Element](media-control.md)                                               |
| 5      | [Informationen zu Callcenter-Steuerelementen](about-call-center-controls.md)                     |
| 6      | [Rendezvous-IP-telefoniekonferenzen](rendezvous-ip-telephony-conferencing.md) |
| 7      | [TAPI Herunterfahren](tapi-shutdown.md)                                               |



 

 

 



