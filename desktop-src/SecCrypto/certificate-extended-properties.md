---
description: Die Daten in einem Zertifikat-, Zertifikatsperrlisten- oder Zertifikatvertrauenslisten-Kontext (Certificate Trust List, CTL), einschließlich erweiterungen, sind schreibgeschützt und können nicht geändert werden.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Erweiterte Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127090"
---
# <a name="certificate-extended-properties"></a>Erweiterte Zertifikateigenschaften

Die Daten in einem [*Zertifikat-,*](../secgloss/c-gly.md) [*Zertifikatsperrlisten-*](../secgloss/c-gly.md) oder [*Zertifikatvertrauenslisten-Kontext*](../secgloss/c-gly.md) (Certificate Trust List, CTL), einschließlich erweiterungen, sind schreibgeschützt und können nicht geändert werden. [](../secgloss/c-gly.md) Auf Microsoft-Plattformen verfügen CryptoAPI-Zertifikate jedoch auch über dynamische erweiterte Eigenschaften, die hinzugefügt und geändert werden können.

> [!Note]  
> Erweiterte Eigenschaften sind einem Zertifikat zugeordnet und nicht Teil eines Zertifikats, wie es von einer [*Zertifizierungsstelle*](../secgloss/c-gly.md) ausgestellt wurde. Erweiterte Eigenschaften sind für ein Zertifikat nicht verfügbar, wenn es auf einer Nicht-Microsoft-Plattform verwendet wird.

 

Zu diesen Eigenschaften gehören Daten, die Folgendes umfassen:

-   Bezieht sich auf den privaten Schlüssel, der mit dem Zertifikat verwendet werden soll.
-   Gibt den Typ der Hashes an, die für das Zertifikat ausgeführt werden sollen.
-   Stellt benutzerdefinierte Informationen bereit, die dem Zertifikat zugeordnet sind.

Auf Microsoft-Plattformen werden Werte für diese Eigenschaften angefügt und mit dem Zertifikat verschoben. Zu den derzeit vordefinierten Eigenschaften, die mit Eigenschaften-IDs identifiziert werden, gehören die folgenden Eigenschaften:

-   Diese Eigenschaften binden ein Zertifikat an einen bestimmten CSP und innerhalb dieses CSP an einen bestimmten privaten Schlüssel:
    -   CERT \_ KEY \_ PROV \_ HANDLE \_ PROP \_ ID
    -   CERT \_ KEY \_ PROV \_ INFO \_ PROP \_ ID
    -   CERT \_ KEY \_ CONTEXT \_ PROP \_ ID
-   Diese Eigenschaften geben den Hashalgorithmus an, der verwendet werden soll, wenn ein Hashvorgang ausgeführt wird:
    -   CERT \_ SHA1 \_ HASH \_ PROP \_ ID
    -   CERT \_ MD5 \_ HASH \_ PROP \_ ID

Vollständige Listen der derzeit definierten erweiterten Zertifikateigenschaften und Beschreibungen der Bedeutung und Verwendung der einzelnen Eigenschaften finden Sie unter [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) und [**CertSetCertificateContextProperty.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
