---
description: Eine Anlagen-Engine ist eine DLL, die dienstspezifische Konfigurations- und Analyseanforderungen verarbeitet.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Anlagen-Engines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e09996bfb58e0447ec8e25bb627af6a4c93751a86f9f73f3499cf7f8b0fdb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895053"
---
# <a name="attachment-engines"></a>Anlagen-Engines

Eine Anlagen-Engine ist eine DLL, die dienstspezifische Konfigurations- und Analyseanforderungen verarbeitet.

Der Benutzer stellt mithilfe der Erweiterung für das Anlagen-Snap-In eine dienstspezifische Konfigurations- und Analyseanforderung. Diese Anforderung wird dann über die Sicherheitskonfigurations-Snap-Ins an die allgemeine Sicherheitskonfigurations-Engine übergeben, die wiederum die dienstspezifische Verarbeitung an die entsprechende Anlagen-Engine übergibt. Die Anlagen-Engine stellt dann eine Verbindung mit dem Dienst her und ändert seine Konfiguration. Anders ausgedrückt: Die Anlagen-Engine stellt die Back-End-Verarbeitung bereit, die die Erweiterung für das Anfüge-Snap-In unterstützt.

Eine Anlagen-Engine muss die folgenden drei Funktionen implementieren:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), das den Unterschied zwischen der Konfiguration des Diensts und der in der Sicherheitsdatenbank gespeicherten Konfiguration berechnet. Die Unterschiede werden in die Sicherheitsdatenbank geschrieben.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), das den Dienst gemäß der Angabe in der Snap-In-Benutzeroberfläche konfiguriert.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), das die Basiskonfiguration und Konfigurationsanalyse für den Dienst in der Sicherheitsdatenbank aktualisiert.

Um die Implementierung der vorherigen Funktionen zu vereinfachen, stellt der Toolsatz für die Sicherheitskonfiguration Unterstützungsfunktionen und Strukturen bereit, die Ihre Anwendung zum Abfragen und Festlegen von Informationen in der Sicherheitsdatenbank verwenden kann. Weitere Informationen finden Sie unter [Attachment Callback Functions](management-functions.md).

Wenn Sie eine Anlagen-Engine-DLL erstellen, müssen Sie sie installieren und dann bei der Sicherheitskonfigurations-Engine registrieren. Um die DLL zu registrieren, fügen Sie der Registrierung einen bestimmten Schlüssel hinzu. Wenn die Sicherheitskonfigurations-Engine gestartet wird, überprüft sie die Registrierung und lädt alle registrierten Anlagen-Engine-DLLs. Anschließend werden dienstspezifische Konfigurations- und Analyseanforderungen an die entsprechende Anlagen-Engine übergeben. Standardkonfigurations- und Analyseanforderungen, die nicht dienstspezifisch sind, werden von der Sicherheitskonfigurations-Engine verarbeitet.

 

 



