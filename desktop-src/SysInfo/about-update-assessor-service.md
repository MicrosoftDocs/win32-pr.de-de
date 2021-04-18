---
description: Im folgenden Thema wird beschrieben, wie die API der Windows as a Service (WAAS) Assessment Platform funktioniert.
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Informationen zur WAAS-Bewertungsplattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351729"
---
# <a name="about-the-waas-assessment-platform"></a>Informationen zur WAAS-Bewertungsplattform

Im folgenden Thema wird beschrieben, wie die API der Windows as a Service (WAAS) Assessment Platform funktioniert.

Die WAAS-Bewertungs-API bietet dem Aufrufer die folgenden Informationen:

-   Wenn ein Gerät auf den neuesten Microsoft-Updates basiert.
-   Gibt an, ob das Gerät das Ende des Supports erreicht hat.
-   Die Releasezeiten für die neuesten anwendbaren Updates für das Gerät.
-   Eine Einschätzung, warum ein Gerät nicht auf dem neuesten Stand ist und welche möglichen Auswirkungen es auf das Gerät haben kann.

Die WAAS Assessment Platform verwendet das com-API-Modell und wird automatisch mindestens einmal pro Tag ausgeführt. Dieser Cycle fängt die anwendbaren Releaseinformationen ab. Im zwischengespeicherten Zeitraum werden für die zwischengespeicherten Releaseinformationen Bewertungen durchgeführt. Wenn ein aufrufen außerhalb des Cache Ablauf Fensters erfolgt, werden ein neuer Rückruf und eine Bewertung durchgeführt, zwischengespeichert und zurückgegeben. Wenn ein-Befehl durchgeführt wird, kontaktiert der WAAS-Bewertungs Client den WAAS-Bewertungs Dienst mit den Attributen des Geräts und empfängt ein auf das Gerät anwendbares Dossier von Informationen. Der Client verwendet diese Informationen dann anhand der Informationen, die er über das Gerät zum Durchführen der Bewertung sammelt.

> [!NOTE]
> Der Code muss über Administratorrechte verfügen, um die WAAS-Bewertungs-API aufzurufen. Weitere Informationen zum Entwickeln von Anwendungen, für die Administratorrechte erforderlich sind, finden Sie in [diesem Artikel](../secauthz/developing-applications-that-require-administrator-privilege.md).

 
