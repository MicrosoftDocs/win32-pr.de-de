---
title: Abfragen ausführlicher Rechte Informationen
description: Abfragen ausführlicher Rechte Informationen
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media-Format-SDK, Abfragen detaillierter Rechte
- Windows Media-Format-SDK, ausführliche Rechte Abfragen
- Digital Rights Management (DRM), Abfragen detaillierter Rechte
- DRM (Digital Rights Management), Abfragen detaillierter Rechte
- Digital Rights Management (DRM), ausführliche Rechte Abfragen
- DRM (Digital Rights Management), ausführliche Rechte Abfragen
- Erweiterte APIs für den DRM-Client, Abfragen detaillierter Rechte
- Erweiterte Client-APIs, Abfragen detaillierter Rechte
- Erweiterte APIs für den DRM-Client, ausführliche Rechte Abfragen
- Erweiterte Client-APIs, ausführliche Rechte Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206859"
---
# <a name="querying-for-detailed-rights-information"></a>Abfragen ausführlicher Rechte Informationen

Mithilfe der [**iwmdrmlicensequery:: querylicenserstate**](iwmdrmlicensequery-querylicensestate.md) -Methode können Sie ausführliche Informationen zu den von den Lizenzen gewährten Rechten für eine Schlüssel-ID abrufen. Die Informationen, die Sie von dieser Methode erhalten, werden von allen Lizenzen im lokalen Lizenz Speicher aggregiert, die auf die angegebene Schlüssel-ID angewendet werden.

**Querylicenserstate** verwendet die [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md) Struktur, um aggregierte Informationen zu allen Lizenzen für die angegebene Schlüssel-ID anzuzeigen. Diese Verwendung unterscheidet sich von anderen Objekten im Windows Media-Format-SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




