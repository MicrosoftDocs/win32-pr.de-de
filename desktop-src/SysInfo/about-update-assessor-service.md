---
description: Im folgenden Thema wird beschrieben, wie die WaaS-Bewertungsplattform-API (Windows-as-a-Service) funktioniert.
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Informationen zur WaaS-Bewertungsplattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79493900d508a8a613953f1f9b7bbd0f67e2a200761148b7fe31d9fb31ce3609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958950"
---
# <a name="about-the-waas-assessment-platform"></a>Informationen zur WaaS-Bewertungsplattform

Im folgenden Thema wird beschrieben, wie die WaaS-Bewertungsplattform-API (Windows-as-a-Service) funktioniert.

Die WaaS-Bewertungs-API bietet dem Aufrufer die folgenden Informationen:

-   Wenn ein Gerät auf den neuesten Microsoft-Updates installiert ist.
-   Gibt an, ob das Gerät das Ende des Supports erreicht hat.
-   Die Releasezeiten für die neuesten anwendbaren Updates für das Gerät.
-   Eine Bewertung, warum ein Gerät nicht auf dem neuesten Stand ist und welche potenziellen Auswirkungen es auf das Gerät haben kann.

Die WaaS-Bewertungsplattform verwendet das COM-API-Modell und wird mindestens einmal täglich automatisch ausgeführt. Dieser Zyklus fängt die entsprechenden Releaseinformationen ab. Während des zwischengespeicherten Zeitraums werden Bewertungen anhand der zwischengespeicherten Releaseinformationen durchgeführt. Wenn ein Aufruf außerhalb des Cacheablauffensters erfolgt, werden ein neuer Aufruf und eine neue Bewertung durchgeführt, zwischengespeichert und zurückgegeben. Wenn ein Aufruf erfolgt, kontaktiert der WaaS-Bewertungsclient den WaaS-Bewertungsdienst mit den Attributen des Geräts und empfängt ein Dossier mit Informationen, die für das Gerät gelten. Der Client verwendet diese Informationen dann anhand der Informationen, die er zum Gerät sammelt, um die Bewertung durchzuführen.

> [!NOTE]
> Ihr Code muss über Administratorrechte verfügen, um die Waas-Bewertungs-API aufzurufen. Weitere Informationen zum Entwickeln von Anwendungen, die Administratorrechte erfordern, finden Sie [in diesem Artikel.](../secauthz/developing-applications-that-require-administrator-privilege.md)

 
