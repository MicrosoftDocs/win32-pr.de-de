---
title: Das Sichere Audiopfadmodell (veraltet)
description: Das Sichere Audiopfadmodell (veraltet)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Medienformat-SDK, Sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), Sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), Sicherer Audiopfad (SAP)
- Microsoft Secure Audio Path (SAP), Modell
- Sicherer Audiopfad (SAP), Modell
- SAP (Sicherer Audiopfad), Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a381d29bcbf4b09ae989325cd5b35c332a6f316c1f932868437ac93a7854ab58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084285"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Das Sichere Audiopfadmodell (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von mit einer anderen technischen Lösung unterstützt Windows.

Microsoft Secure Audio Path (SAP) ist ein Feature von Microsoft Windows® Me und Microsoft Windows XP. Die Anforderung, dass eine Audiodatei nur über einen sicheren Audiopfad abgespielt werden muss, wird in der DRM-Lizenz angegeben und von den DRM-Clientkomponenten erzwungen. Für nur SAP-Dateien wurde keine zusätzliche Verschlüsselung hinzugefügt, wenn sie anfänglich geschützt sind. Die SAP-Verschlüsselung wird von den DRM-Komponenten zur Wiedergabezeit automatisch hinzugefügt, ebenso wie der Authentifizierungsprozess für alle Softwarekomponenten, die an der Wiedergabe beteiligt sind. Die Arbeitsmöglichkeiten von SAP sind daher für Anwendungen vollständig transparent, und aus diesem Grund gibt es keine Methode oder Eigenschaft im Windows Media Format SDK zum Aktivieren oder Deaktivieren von SAP. Bei Bedarf kann ein Inhaltsbesitzer beim Erstellen einer geschützten Datei ein benutzerdefiniertes Headerattribut namens "DRMHeader.SAPRequired" hinzufügen, um einen Lizenzserver anweisen zu lassen, der Lizenz die SAP-Anforderung hinzuzufügen. Die Implementierung eines solchen Schemas liegt beim Inhaltsbesitzer und beim Lizenzdienst.

Wenn im aktuellen DRM-Modell SAP nicht angewendet wird und geschützte digitale Musik abgespielt wird, werden die verschlüsselten Inhalte an die DRM-Clientkomponente übertragen. Der DRM-Client überprüft, ob die Anwendung und die DRM-Komponente, die das Windows Media Format SDK enthält, gültig sind. Wenn sie gültig sind, entschlüsselt der DRM-Client den Inhalt und sendet ihn an die Anwendung, die ihn dann an die Niedrigeren Audiokomponenten sendet. An diesem Punkt ist die entschlüsselte Musik für Benutzermodusanwendungen und Plug-Ins und Kernelmodustreiber verfügbar, die die entschlüsselten Audiobits abfangen können.

Wenn die Anforderung sicherer Audiopfade angewendet wird, wird der Inhalt nicht von der Anwendung entschlüsselt, sondern in einem verschlüsselten Zustand an Komponenten auf niedrigerer Ebene übergeben, die alle von Microsoft als vertrauenswürdig authentifiziert wurden. Bei einer vertrauenswürdigen Audiokomponente handelt es sich um eine Komponente, die den Audioinhalt nur für andere spezifische vertrauenswürdige Komponenten verfügbar macht. Auf diese Weise bleiben die digitalen Inhalte bis zur Treiberebene geschützt.

Das folgende Diagramm zeigt das aktuelle Modell im Vergleich zum Modell "Sicherer Audiopfad".

![Diagramm des sicheren Audiopfadmodells](images/sap.png)

 

 




