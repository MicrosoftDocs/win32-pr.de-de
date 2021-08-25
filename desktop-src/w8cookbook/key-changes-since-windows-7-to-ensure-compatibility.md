---
title: Wichtige Änderungen seit Windows 7, um die Kompatibilität sicherzustellen
description: Wichtige Änderungen seit Windows 7, um die Kompatibilität sicherzustellen
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ed00dacb0d8556d4e16de84fbc20b7ac6a56bed6560bee3213c7919b9760cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815190"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a>Wichtige Änderungen seit Windows 7, um die Kompatibilität sicherzustellen

Kompatibilität hat für Entwickler einen hohen Stellenwert. ISVs und Entwickler möchten sicherstellen, dass ihre Apps unter allen unterstützten Versionen des Windows-Betriebssystems erwartungsgemäß ausgeführt werden. Verbraucher und Unternehmen haben ebenfalls ein Interesse daran, dass die von ihnen erworbenen Apps weiterhin funktionieren. Wir wissen, dass Kompatibilität das Hauptkriterium für die Kaufentscheidung ist. Apps, die basierend auf bewährten Methoden gut geschrieben sind, führen zu einer deutlich geringeren Codeänderungsrate, wenn eine neue Windows Version veröffentlicht wird, und verringern die Fragmentierung– diese Apps verfügen über eine geringere Entwicklungsinvestitionen und eine schnellere Markteinführungszeit.

Zu Zeiten von Windows 7 ging es vielmehr darum, auf Kompatibilitätsprobleme zu reagieren. In Windows 8 haben wir umgedacht und direkt innerhalb des Windows-Betriebssystems und nicht erst im Nachhinein für Kompatibilität gesorgt. Windows 10 ist entwurfsbedingt die bisher kompatibelste Betriebssystemversion. Einige wichtige Aspekte, die uns bei der Umsetzung geholfen haben:

-   App-Telemetrie: Dies hilft uns, die Beliebtheit von Apps im Windows Ökosystem zu verstehen, um Kompatibilitätstests zu unterstützen.
-   ISV-Partnerschaften: Arbeiten Sie direkt mit externen Partnern zusammen, um ihnen Daten bereitzustellen und Probleme zu beheben, die für unsere Benutzer auftreten.
-   Entwurfsüberprüfungen, Upstreamerkennung: Arbeiten Sie mit Featureteams zusammen, um die Anzahl breaking changes in Windows zu reduzieren. Kompatibilitätsprüfungen sind für jedes Featureteam ein Muss.
-   Strengere Kontrolle über API-Änderungen & verbesserte Kommunikation
-   Flighting- und Feedbackschleife: Die Windows Insider-Population empfängt flighted-Builds, die unsere Fähigkeit verbessern, Kompatibilitätsprobleme zu finden, bevor ein finaler Build für Kunden freigegeben wird. Unser Feedbackverfahren sorgt nicht nur für die Fehlererkennung, sondern auch dafür, dass Benutzer die Features erhalten, die sie brauchen.

 

 




