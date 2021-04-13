---
title: Das sichere Audiopfad-Modell (veraltet)
description: Das sichere Audiopfad-Modell (veraltet)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Microsoft Secure-Audiopfad (SAP), Modell
- Sicherer Audiopfad (SAP), Modell
- SAP (sicherer Audiopfad), Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388204"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Das sichere Audiopfad-Modell (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.

Microsoft Secure-Audiopfad (SAP) ist ein Feature von Microsoft Windows® Me und Microsoft Windows XP. Die Anforderung, dass eine Audiodatei nur über einen sicheren Audiopfad abgespielt werden soll, wird in der DRM-Lizenz angegeben und durch die DRM-Client Komponenten erzwungen. Es wird keine zusätzliche Verschlüsselung für reine SAP-Dateien hinzugefügt, wenn Sie anfänglich geschützt werden. Die SAP-Verschlüsselung wird von den DRM-Komponenten zur Wiedergabezeit automatisch hinzugefügt, ebenso wie der Authentifizierungsprozess für alle Softwarekomponenten, die an der Wiedergabe beteiligt sind. Die Funktionsweise von SAP ist daher für Anwendungen vollständig transparent, und aus diesem Grund gibt es keine Methode oder Eigenschaft im Windows Media-Format-SDK zum Aktivieren oder Deaktivieren von SAP. Wenn gewünscht, kann ein Inhalts Besitzer beim Erstellen einer geschützten Datei ein benutzerdefiniertes Header Attribut mit dem Namen "drmHeader. saprequired" hinzufügen, um einen Lizenzserver anzuweisen, die SAP-Anforderung der Lizenz hinzuzufügen. Die Implementierung eines solchen Schemas ist der Besitzer des Inhalts und der Lizenz Dienst.

Wenn beim aktuellen DRM-Modell SAP nicht angewendet wird, wird der verschlüsselte Inhalt bei der Wiedergabe geschützter digitaler Musik an die DRM-Client Komponente weitergegeben. Der DRM-Client überprüft, ob die Anwendung und die DRM-Komponente, die das Windows Media Format SDK umfasst, gültig sind. Wenn Sie gültig sind, entschlüsselt der DRM-Client den Inhalt und sendet ihn an die Anwendung, die ihn dann an die untergeordneten Audiokomponenten sendet. An diesem Punkt ist die entschlüsselte Musik für Benutzermodusanwendungen und Plug-ins und Kernelmodustreiber verfügbar, die die entschlüsselten audiobits abfangen können.

Wenn die Anforderung für den sicheren Audiopfad angewendet wird, wird der Inhalt nicht von der Anwendung entschlüsselt, sondern stattdessen in einem verschlüsselten Zustand an Komponenten auf niedrigerer Ebene, die alle von Microsoft als vertrauenswürdig authentifiziert wurden. Eine vertrauenswürdige Audiokomponente ist eine, die den Audioinhalt nicht für eine Systemkomponente verfügbar macht, außer für andere bestimmte vertrauenswürdige Komponenten. Auf diese Weise bleibt der digitale Inhalt bis hin zur Treiber Ebene geschützt.

Im folgenden Diagramm wird das aktuelle Modell im Vergleich zum sicheren Audiopfad-Modell angezeigt.

![Diagramm des sicheren Audiopfad Modells](images/sap.png)

 

 




