---
description: Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Zuordnen Xenroll.dll zu CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8cd2286823dbf8029896c8656807f614dc0e1994fda908cd9b13ec8ad24c7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993529"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Zuordnen Xenroll.dll zu CertEnroll.dll

Vor Windows Vista wurde die Zertifikatregistrierungssteuerung in Xenroll.dll implementiert. Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.

Xenroll hat versucht, zwei parallele Sätze von Schnittstellen zu implementieren. [**ICEnroll,**](/windows/desktop/api/xenroll/nn-xenroll-icenroll) [**ICEnroll2,**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2) [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)und [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) waren Automation-kompatibel und mit Skriptsprachen kompatibel. Die entsprechenden Schnittstellen [**– IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)und [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)– konnten nicht mit Skripts erstellt werden, waren aber für C++-Programmierer praktischer. Während sie sich entwickelt haben, bleiben die beiden Schnittstellensätze nicht synchronisiert. Insbesondere definiert der Satz von dualen Schnittstellen, die zuletzt durch **ICEnroll4** dargestellt wurden, nur eine Teilmenge der von **IEnroll4 definierten** Funktionalität.

CertEnroll.dll implementiert einen größeren und strukturierteren Satz automatisierungskonformer COM-Schnittstellen. In den folgenden Themen wird erläutert, wie Xenroll.dll CertEnroll.dll für verschiedene Arten von Funktionen zugeordnet wird.

-   [Zertifikatanforderungsfunktionen](certificate-request-functions.md)
-   [Zertifikatantwortfunktionen](certificate-response-functions.md)
-   [Attributfunktionen](attribute-functions.md)
-   [Erweiterungsfunktionen](extension-functions.md)
-   [Externe Eigenschaftenfunktionen](external-property-functions.md)
-   [Funktionen für private und öffentliche Schlüssel](private-and-public-key-functions.md)
-   [Kryptografiedienstanbieterfunktionen](cryptographic-service-provider-functions.md)
-   [Certificate Store Functions](certificate-store-functions.md)
-   [Persönliche Informationen Exchange Functions](personal-information-exchange-functions.md)
-   [Hilfsfunktionen](helper-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
