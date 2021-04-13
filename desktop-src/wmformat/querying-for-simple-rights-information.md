---
title: Abfragen von einfachen Rechte Informationen
description: Abfragen von einfachen Rechte Informationen
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media-Format-SDK, Abfragen für einfache Rechte
- Windows Media-Format-SDK, einfache Rechte Abfragen
- Digital Rights Management (DRM), Abfragen für einfache Rechte
- DRM (Digital Rights Management), Abfragen für einfache Rechte
- Digital Rights Management (DRM), einfache Rechte Abfragen
- DRM-Abfragen (Digital Rights Management), einfache Rechte Abfragen
- Erweiterte APIs für den DRM-Client, Abfragen für einfache Rechte
- Erweiterte Client-APIs, Abfragen für einfache Rechte
- Erweiterte APIs für den DRM-Client, einfache Rechte Abfragen
- Erweiterte Client-APIs, einfache Rechte Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388323"
---
# <a name="querying-for-simple-rights-information"></a>Abfragen von einfachen Rechte Informationen

Mit den erweiterten APIs für den Windows Media DRM-Client können Sie schnell einfache Informationen über den Zugriff auf geschützte Inhalte für verschiedene Aktionen erhalten.

Die [**iwmdrmlicensequery:: queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Methode kann verwendet werden, um schnell festzustellen, ob eine Aktion durch eine Lizenz im lokalen Lizenz Speicher zulässig ist. **Queryaktionallowed** wurde so optimiert, dass es viel schneller als Abfragen für ähnliche Informationen ist, indem die Objekte des Windows Media Format SDK verwendet werden. Diese Art von Abfrage aggregiert jedoch die Lizenzen im lokalen Lizenz Speicher und sollte nur für einfache Features verwendet werden, z. b. für Elemente der Benutzeroberfläche, z. b. für die Anzeige eines Berechtigungs Indikators.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




