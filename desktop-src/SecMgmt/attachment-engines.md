---
description: Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Anlagen-Engines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866963"
---
# <a name="attachment-engines"></a>Anlagen-Engines

Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet.

Der Benutzer stellt eine Dienst spezifische Konfigurations-und Analyse Anforderung mithilfe der Erweiterungs-Snap-in-Erweiterung her. Diese Anforderung wird dann über die Sicherheitskonfigurations-Snap-Ins an die allgemeine Sicherheitskonfigurations-Engine weitergeleitet, die wiederum die Dienst spezifische Verarbeitung an die entsprechende Anlage-Engine übergibt. Die Anlagen-Engine stellt dann eine Verbindung mit dem Dienst her und ändert seine Konfiguration. Mit anderen Worten: die Anlagen-Engine stellt die Back-End-Verarbeitung bereit, die die Erweiterungs-Snap-in-Erweiterung unterstützt.

Eine Anlage-Engine muss die folgenden drei Funktionen implementieren:

-   [**Scesvstreamtachmentanalysis**](scesvcattachmentanalyze.md): berechnet den Unterschied zwischen der Konfiguration des Diensts und der Konfiguration, die in der Sicherheitsdatenbank gespeichert ist. Die Unterschiede werden in die Sicherheitsdatenbank geschrieben.
-   [**Scesvtortachmentconfig**](scesvcattachmentconfig.md): Hiermit wird der Dienst entsprechend der Angabe in der Snap-in-Benutzeroberfläche konfiguriert.
-   [**Scesvsintachmentupdate**](scesvcattachmentupdate.md), das die Basiskonfiguration und Konfigurations Analyse für den Dienst in der Sicherheitsdatenbank aktualisiert.

Um die Implementierung der vorangehenden Funktionen zu vereinfachen, stellt das Sicherheitskonfigurations-Toolset Unterstützungsfunktionen und-Strukturen bereit, die Ihre Anwendung zum Abfragen und Festlegen von Informationen in der Sicherheitsdatenbank verwenden kann. Weitere Informationen finden Sie unter [Anlage Rückruf Funktionen](management-functions.md).

Wenn Sie eine Anlagen-Engine-dll erstellen, müssen Sie Sie installieren und anschließend bei der Sicherheitskonfigurations-Engine registrieren. Um die dll zu registrieren, fügen Sie der Registrierung einen bestimmten Schlüssel hinzu. Beim Start der Sicherheitskonfigurations-Engine wird die Registrierung überprüft und alle registrierten Anlagen-Engine-DLLs geladen. Anschließend werden Dienst spezifische Konfigurations-und Analyseanforderungen an die entsprechende Anlage-Engine weitergeleitet. Standard Konfigurations-und Analyseanforderungen, die nicht Dienst spezifisch sind, werden von der Sicherheitskonfigurations-Engine verarbeitet.

 

 



