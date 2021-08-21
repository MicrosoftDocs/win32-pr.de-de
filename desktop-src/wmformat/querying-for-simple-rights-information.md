---
title: Abfragen einfacher Rechteinformationen
description: Abfragen einfacher Rechteinformationen
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Medienformat-SDK, Abfragen einfacher Rechte
- Windows Medienformat-SDK, einfache Rechteabfragen
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Abfragen einfacher Rechte
- DRM (Digital Rights Management), Abfragen einfacher Rechte
- Digital Rights Management (DRM), einfache Rechteabfragen
- DRM (Digital Rights Management), einfache Rechteabfragen
- Erweiterte DRM-Client-APIs, Abfragen einfacher Rechte
- Erweiterte Client-APIs, Abfragen einfacher Rechte
- ERWEITERTE APIs für DEN DRM-Client, einfache Rechteabfragen
- Erweiterte Client-APIs, einfache Rechteabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0686616bbc700c51a005c3e1e63eed889c42965aaebbba232fcf90b9cce26987
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027368"
---
# <a name="querying-for-simple-rights-information"></a>Abfragen einfacher Rechteinformationen

Die Windows Media DRM Client Extended APIs ermöglichen es Ihnen, schnell einfache Informationen darüber zu erhalten, ob auf geschützte Inhalte für verschiedene Aktionen zugegriffen werden kann.

Die [**IWMDRMLicenseQuery::QueryActionAllowed-Methode**](iwmdrmlicensequery-queryactionallowed.md) kann verwendet werden, um schnell zu bestimmen, ob eine Aktion von einer Lizenz im lokalen Lizenzspeicher zugelassen wird. **QueryActionAllowed** wurde optimiert, um viel schneller als Abfragen für ähnliche Informationen mithilfe der Objekte des Windows Media Format SDK zu sein. Diese Art von Abfrage aggregiert jedoch die Lizenzen im lokalen Lizenzspeicher und sollte nur für einfache Features verwendet werden, z. B. für Benutzeroberflächenelemente, z. B. das Anzeigen eines Berechtigungsindikators.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Abrufen von Informationen aus Lizenzen im lokalen Store**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




