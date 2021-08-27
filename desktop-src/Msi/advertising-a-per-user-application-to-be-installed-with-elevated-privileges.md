---
description: 'Um eine Anwendung auf Benutzerbasis anzukündigen, wenn die Anwendung erhöhte Berechtigungen (d. b. Systemberechtigungen) für die Installation benötigt, verwenden Sie die Richtlinien in der folgenden Liste:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Ananzeigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdced246f90a345b5b2cc599541119a26e29e4d9a1d708be1ee8299d55d3c28d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082960"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Ananzeigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll

Um eine Anwendung auf Benutzerbasis anzukündigen, wenn die Anwendung erhöhte Berechtigungen (d. b. Systemberechtigungen) für die Installation benötigt, verwenden Sie die Richtlinien in der folgenden Liste:

-   Ihr Prozess muss ein Dienst sein, der unter dem Systemkonto LocalSystem auf Windows XP oder höher ausgeführt wird.
-   Generieren Sie ein Ankündigen eines Skripts, indem [**Sie MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) oder [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)aufrufen.
-   Ihr Prozess muss die Identität des Benutzers annehmen, der das Ziel für die Ankündigung ist.
-   Rufen Sie [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)auf, und verwenden Sie die Flags SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| SCRIPTFLAGS \_ REGDATA \_ CNFGINFO \| SCRIPTFLAGS \_ SHORTCUTS.

Wenn Sie die Richtlinien befolgen, kündigen Sie eine Anwendung für einen angegebenen Benutzer an, und wenn der Benutzer sich für die Installation entscheidet, wird die Anwendung mit erhöhten Rechten installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen von verwalteten Anwendungen pro Benutzer](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



