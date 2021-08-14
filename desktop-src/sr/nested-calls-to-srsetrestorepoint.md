---
title: Geschachtelte Aufrufe von SRSetRestorePoint
description: In diesem Thema wird die Unterstützung für geschachtelte Aufrufe von SRSetRestorePoint über die Ereignistypen BEGIN \_ NESTED \_ SYSTEM CHANGE und \_ END \_ NESTED SYSTEM CHANGE \_ \_ beschrieben.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12286a69bdb83cb5fd119280e8996c6612e359bf93b9371b6a088a98bf6fd881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857635"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Geschachtelte Aufrufe von SRSetRestorePoint

In diesem Thema wird die Unterstützung für geschachtelte Aufrufe von [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) über die Ereignistypen BEGIN \_ NESTED \_ SYSTEM CHANGE und \_ END \_ NESTED SYSTEM CHANGE \_ \_ beschrieben.

Anwendungen können [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) sicher aufrufen, wenn diese Ereignistypen verwendet werden. Der erste Aufruf der Funktion erstellt einen Wiederherstellungspunkt. Nachfolgende geschachtelte Aufrufe der Funktion erstellen keine Wiederherstellungspunkte. Angenommen, eine Anwendung ruft **SRSetRestorePoint** wie folgt auf:<dl> Für Wiederherstellungspunkt A mit dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Für Wiederherstellungspunkt B mit dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Für Wiederherstellungspunkt B mit dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
Für Wiederherstellungspunkt A mit dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
</dl>

Der zweite Aufruf erstellt keinen neuen Wiederherstellungspunkt, da der Aufruf geschachtelt ist.

 

 




