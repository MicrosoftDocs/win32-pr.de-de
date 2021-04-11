---
title: Aufgerufenen Aufrufe von srsettrestorepoint
description: In diesem Thema wird die Unterstützung für die Verwendung von nsted-Aufrufen von SRSetRestorePoint durch die Ereignis Typen "geänderter \_ \_ System \_ Änderungs Vorgang und-Ende- \_ \_ System \_ Änderung" beschrieben
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206862"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Aufgerufenen Aufrufe von srsettrestorepoint

In diesem Thema wird die Unterstützung für die Verwendung von nsted-Aufrufen von [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) durch die Ereignis Typen "geänderter \_ \_ System \_ Änderungs Vorgang und-Ende- \_ \_ System \_ Änderung" beschrieben

Anwendungen können [**srtartrestorepoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) bei Verwendung dieser Ereignis Typen sicher aufzurufen. Der erste Aufrufe der-Funktion erstellt einen Wiederherstellungspunkt. Nachfolgende, in der Funktion ausgehosterte Aufrufe erstellen keine Wiederherstellungspunkte. Nehmen Sie z. b. an, eine Anwendung führt die folgenden Aufrufe von **SRSetRestorePoint** aus:<dl> Für Wiederherstellungspunkt A mit dwEventType = geänderte \_ \_ System \_ Änderung starten  
Für Wiederherstellungspunkt B mit dwEventType = \_ \_ System Änderung für \_ "Anfang"  
Für Wiederherstellungspunkt B mit dwEventType = \_ \_ System Änderung am Ende des Systems \_  
Für Wiederherstellungspunkt A mit dwEventType = \_ \_ System Änderung am Ende des Systems \_  
</dl>

Beim zweiten-Befehl wird kein neuer Wiederherstellungspunkt erstellt, da der-aufzurufende aufgerufen wird.

 

 




