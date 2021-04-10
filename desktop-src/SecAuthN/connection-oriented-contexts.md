---
description: Bei einem Verbindungs orientierten Kontext ist der Aufrufer der Funktion für das Formatieren von Nachrichten verantwortlich. Der Aufrufer basiert auf dem Sicherheitspaket zum Authentifizieren von Verbindungen und zur Gewährleistung der Integrität bestimmter Teile der Nachricht.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Connection-Oriented Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131053"
---
# <a name="connection-oriented-contexts"></a>Connection-Oriented Kontexte

Bei einem Verbindungs orientierten [*Kontext*](/windows/desktop/SecGloss/c-gly)ist der Aufrufer der Funktion für das Formatieren von Nachrichten verantwortlich. Der Aufrufer basiert auf dem [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) zum Authentifizieren von Verbindungen und zur Gewährleistung der Integrität bestimmter Teile der Nachricht.

Die meisten Kontextoptionen sind für Verbindungs orientierte Kontexte verfügbar. Zu diesen Optionen zählen die gegenseitige Authentifizierung, Wiedergabe Erkennung und Sequenz Erkennung, wie in den [Kontext Anforderungen](context-requirements.md)beschrieben.

Ein Sicherheitspaket legt das secpkg- \_ Flag \_ -verbindungsflag fest, um anzugeben, dass es die Verbindungs orientierte Semantik unterstützt.

 

 
