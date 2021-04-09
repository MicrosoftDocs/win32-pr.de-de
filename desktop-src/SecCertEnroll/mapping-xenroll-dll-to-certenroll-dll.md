---
description: Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Zuordnung von Xenroll.dll zu CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758059"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Zuordnung von Xenroll.dll zu CertEnroll.dll

Vor Windows Vista wurde die Zertifikat Registrierungs Steuerung in Xenroll.dll implementiert. Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.

XEnroll versuchte, zwei parallele Sätze von Schnittstellen zu implementieren. [**Icenroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)und [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) waren Automatisierungs konform und kompatibel mit Skriptsprachen. Die entsprechenden Schnittstellen –[**ienroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)und [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)– konnten nicht in die Skripterstellung einbezogen werden, wurden jedoch für C++ Programmierer besser geeignet. Wenn Sie sich entwickelt haben, wurden die beiden Schnittstellen Sätze nicht synchronisiert. Insbesondere definiert der Satz von Dual Schnittstellen, der von **ICEnroll4** zuletzt dargestellt wird, nur eine Teilmenge der von **IEnroll4** definierten Funktionen.

CertEnroll.dll implementiert einen größeren und strukturierteren Satz von Automatisierungs kompatiblen com-Schnittstellen. In den folgenden Themen wird erläutert, wie Xenroll.dll CertEnroll.dll für verschiedene Funktionstypen zuordnet.

-   [Zertifikat Anforderungs Funktionen](certificate-request-functions.md)
-   [Funktionen für Zertifikat Antworten](certificate-response-functions.md)
-   [Attribut Funktionen](attribute-functions.md)
-   [Erweiterungsfunktionen](extension-functions.md)
-   [Externe Eigenschaften Funktionen](external-property-functions.md)
-   [Funktionen für private und öffentliche Schlüssel](private-and-public-key-functions.md)
-   [Kryptografiedienstanbieter-Funktionen](cryptographic-service-provider-functions.md)
-   [Zertifikat Speicherfunktionen](certificate-store-functions.md)
-   [Funktionen für den persönlichen Informationsaustausch](personal-information-exchange-functions.md)
-   [Hilfsfunktionen](helper-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
