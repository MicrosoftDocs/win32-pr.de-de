---
title: Individualisieren von DRM-Anwendungen
description: Individualisieren von DRM-Anwendungen
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media-Format-SDK, Individualisieren von DRM-Anwendungen
- Windows Media-Format-SDK, Anwendungs Individualisierung
- Advanced Systems Format (ASF), Individualisieren von DRM-Anwendungen
- ASF (Advanced Systems Format), Individualisieren von DRM-Anwendungen
- Advanced Systems Format (ASF), Anwendungs Individualisierung
- ASF (Advanced Systems Format), Anwendungs Individualisierung
- Digital Rights Management (DRM), Individual Anwendungen
- DRM (Digital Rights Management), Individual Anwendungen
- Digital Rights Management (DRM), Anwendungs Individualisierung
- DRM (Digital Rights Management), Anwendungs Individualisierung
- Anwendungs Individualisierung
- Individualisieren von DRM-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103948502"
---
# <a name="individualizing-drm-applications"></a>Individualisieren von DRM-Anwendungen

Um die Sicherheit zu erhöhen, kann die DRM-Komponente der Anwendungen *individuell individualisiert* werden. Eine individualisierte Anwendung ist eine Anwendung, die ein Upgrade auf die DRM-Komponenten erhalten hat, die Sie von allen anderen Kopien der gleichen Anwendung unterscheiden. Inhalts Besitzer können verlangen, dass Ihre geschützten Dateien nur in einer Anwendung wiedergegeben werden, die individuell ist.

Der Individualisierungsprozess wird gestartet, wenn die Anwendung den Microsoft-Individualisierungs Dienst kontaktiert, der dann ein Sicherheits Upgrade auf dem Computer des Benutzers installiert. Da der Individualisierungs Dienst Informationen vom Benutzer verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website angeben: <https://privacy.microsoft.com/privacystatement> .

Die Individualisierung kann auf unterschiedliche Weise durchgeführt werden. So kann z. b. eine Individualisierung erfolgen, wenn ein Benutzer eine geschützte Datei spielt. Die Lizenz Anforderung wird an den [*Windows Media License Service*](wmformat-glossary.md)gesendet, der das Zertifikat der Anwendung überprüft, die die [*Lizenz*](wmformat-glossary.md)anfordert. Wenn die DRM-Komponente der Anwendung nicht individualisiert wurde, lehnt der Windows Media License Service die Lizenz ab, da es sich hierbei um die Richtlinie von Windows Media License Service handelt, die nur für individualisierte Spieler Lizenzen ausgibt. Die Anwendung kann dann den Benutzer benachrichtigen, dass ein Upgrade der Anwendung ausgeführt werden muss. Wenn der Benutzer zustimmt, wird ein Sicherheits Upgrade bereitgestellt, um die DRM-Komponente der Anwendung zu individualisieren.

Um eine bessere Benutzer Leistung zu erzielen, können Sie den Individualisierungsprozess während des Setups als Sicherheits upgradeschritt initiieren. Anschließend wird der Benutzer nicht unterbrochen, um beim Versuch, eine geschützte Datei wiederzugeben, ein Sicherheits Upgrade zu erhalten. Sie können die Individualisierung auch durch Hinzufügen eines Menübefehls oder einer Schaltfläche zur **Sicherheitsaktualisierung** zur Anwendung aktiv fördern.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




