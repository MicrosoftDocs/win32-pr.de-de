---
title: Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten
description: Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310848"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a>Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten

Kompatibilität hat für Entwickler einen hohen Stellenwert. ISVs und Entwickler möchten sicherstellen, dass ihre Apps unter allen unterstützten Versionen des Windows-Betriebssystems erwartungsgemäß ausgeführt werden. Verbraucher und Unternehmen haben ebenfalls ein Interesse daran, dass die von ihnen erworbenen Apps weiterhin funktionieren. Wir wissen, dass Kompatibilität das Hauptkriterium für die Kaufentscheidung ist. Apps, die basierend auf bewährten Methoden ordnungsgemäß geschrieben werden, führen zu einer deutlich geringeren Codeänderung, wenn eine neue Windows-Version veröffentlicht wird. Dadurch wird die Fragmentierung reduziert – diese apps haben eine reduzierte Entwicklungs Investition und eine schnellere Markteinführungszeit.

Zu Zeiten von Windows 7 ging es vielmehr darum, auf Kompatibilitätsprobleme zu reagieren. In Windows 8 haben wir umgedacht und direkt innerhalb des Windows-Betriebssystems und nicht erst im Nachhinein für Kompatibilität gesorgt. Windows 10 ist entwurfsbedingt die bisher kompatibelste Betriebssystemversion. Einige wichtige Aspekte, die uns bei der Umsetzung geholfen haben:

-   App-Telemetrie: Dies hilft uns, die Beliebtheit von apps im Windows-Ökosystem zu verstehen, um Kompatibilitätstests zu informieren.
-   ISV-Partnerschaften: Arbeiten Sie direkt mit externen Partnern zusammen, um Ihnen Daten bereitzustellen und Probleme zu beheben, die unsere Benutzer haben.
-   Entwurfs Überprüfungen, Upstream-Erkennung: Partner mit Featureteams, um die Anzahl der wichtigen Änderungen in Windows zu verringern. Kompatibilitätsprüfungen sind für jedes Featureteam ein Muss.
-   Strengere Kontrolle über API-Änderungen & verbesserte Kommunikation
-   Flighting-und Feedback Schleife: die Windows Insider Population erhält geflistete Builds, die zur Verbesserung unserer Fähigkeit zum Auffinden von Kompatibilitätsproblemen beitragen, bevor ein endgültiger Build für Kunden veröffentlicht wird. Unser Feedbackverfahren sorgt nicht nur für die Fehlererkennung, sondern auch dafür, dass Benutzer die Features erhalten, die sie brauchen.

 

 




