---
title: Individualisieren von DRM-Anwendungen
description: Individualisieren von DRM-Anwendungen
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Medienformat-SDK, Individualisieren von DRM-Anwendungen
- Windows Medienformat-SDK, Individualisierung der Anwendung
- Advanced Systems Format (ASF), Individualisieren von DRM-Anwendungen
- ASF (Advanced Systems Format), Individualisieren von DRM-Anwendungen
- Advanced Systems Format (ASF), Individualisieren von Anwendungen
- ASF (Advanced Systems Format), Individualisieren von Anwendungen
- Digital Rights Management (DRM), Individualisieren von Anwendungen
- DRM (Digital Rights Management), Individualisieren von Anwendungen
- Digital Rights Management (DRM), Individualisierung von Anwendungen
- DRM (Digital Rights Management), Individualisierung von Anwendungen
- Individualisierung der Anwendung
- Individualisieren von DRM-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c57b6f884e2304508243180cc536899f991b1baab6f7f540f04f12fb805d6f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809020"
---
# <a name="individualizing-drm-applications"></a>Individualisieren von DRM-Anwendungen

Um die Sicherheit zu erhöhen, kann die DRM-Komponente von Anwendungen *individualisiert* werden. Eine individualisierte Anwendung ist eine Anwendung, die ein Upgrade auf ihre DRM-Komponenten erhalten hat, die sie von allen anderen Kopien derselben Anwendung unterscheidet. Inhaltsbesitzer können verlangen, dass ihre geschützten Dateien nur in einer Anwendung wiedergegeben werden, die individualisiert wurde.

Der Individualisierungsprozess wird gestartet, wenn die Anwendung den Microsoft Individualization Service kontaktiert, der dann ein Sicherheitsupgrade auf dem Computer des Benutzers installiert. Da der Individualisierungsdienst Informationen des Benutzers verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website bereitstellen: <https://privacy.microsoft.com/privacystatement> .

Die Individualisierung kann auf unterschiedliche Weise erfolgen. Die Individualisierung kann beispielsweise erfolgen, wenn ein Benutzer eine geschützte Datei wiedergibt. Die Lizenzanforderung wird an den [*Windows Media License Service*](wmformat-glossary.md)gesendet, der das Zertifikat der Anwendung überprüft, die die [*Lizenz*](wmformat-glossary.md)anfordert. Wenn die DRM-Komponente der Anwendung nicht individualisiert wurde, lehnt Windows Media License Service die Lizenz aus, da es die Richtlinie von Windows Media License Service ist, Lizenzen nur für individualisierte Player auszustellen. Die Anwendung kann den Benutzer dann benachrichtigen, dass ein Upgrade der Anwendung durchgeführt werden muss. Wenn der Benutzer zustimmt, wird ein Sicherheitsupgrade bereitgestellt, um die DRM-Komponente der Anwendung zu individualisieren.

Um die Benutzerfreundlichkeit zu verbessern, können Sie den Individualisierungsprozess während des Setups als Sicherheitsupgradeschritt initiieren. dann wird der Benutzer nicht unterbrochen, um beim Versuch, eine geschützte Datei wiederzuspielen, ein Sicherheitsupgrade zu erhalten. Sie können die Individualisierung auch aktiv fördern, indem Sie der Anwendung einen Menübefehl oder eine Schaltfläche für das **Sicherheitsupgrade** hinzufügen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




