---
description: Die Daten in einem Zertifikat, einer Zertifikat Sperr Liste oder einem CTL (Certificate Trust List)-Kontext, einschließlich Erweiterungen, sind schreibgeschützt und können nicht geändert werden.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Erweiterte Zertifikat Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131052"
---
# <a name="certificate-extended-properties"></a>Erweiterte Zertifikat Eigenschaften

Die Daten in einem [*Zertifikat*](../secgloss/c-gly.md), einer Zertifikat Sperr [*Liste*](../secgloss/c-gly.md) oder einem CTL ( [*Certificate Trust List*](../secgloss/c-gly.md) )- [*Kontext*](../secgloss/c-gly.md), einschließlich Erweiterungen, sind schreibgeschützt und können nicht geändert werden. Auf Microsoft-Plattformen verfügen CryptoAPI-Zertifikate jedoch auch über dynamische erweiterte Eigenschaften, die hinzugefügt und geändert werden können.

> [!Note]  
> Erweiterte Eigenschaften werden einem Zertifikat zugeordnet und sind nicht Teil eines Zertifikats, das von einer Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) ausgestellt wurde. Erweiterte Eigenschaften sind für ein Zertifikat nicht verfügbar, wenn es auf einer anderen Plattform als Microsoft verwendet wird.

 

Zu diesen Eigenschaften zählen folgende Daten:

-   Bezieht sich auf den privaten Schlüssel, der mit dem Zertifikat verwendet werden soll.
-   Gibt den Typ der Hashes an, die für das Zertifikat ausgeführt werden sollen.
-   Stellt benutzerdefinierte Informationen bereit, die dem Zertifikat zugeordnet sind.

Auf Microsoft-Plattformen werden Werte für diese Eigenschaften angefügt und mit dem Zertifikat verschoben. Aktuell vordefinierte Eigenschaften, die mit Eigenschaften-IDs identifiziert werden, enthalten die folgenden Eigenschaften:

-   Mit diesen Eigenschaften wird ein Zertifikat mit einem bestimmten CSP und innerhalb des CSP mit einem bestimmten privaten Schlüssel verknüpft:
    -   Stamm-ID des CERT \_ Key- \_ Prov- \_ Handles \_ \_
    -   Zertifikat \_ Schlüssel- \_ Prov- \_ \_ Infoprop- \_ ID
    -   CERT \_ Key- \_ Kontext-Prop- \_ \_ ID
-   Diese Eigenschaften geben den Hash Algorithmus an, der verwendet werden soll, wenn ein Hash Vorgang durchgeführt wird:
    -   CERT \_ SHA1- \_ Hashwert- \_ \_ ID
    -   Zertifikat- \_ MD5- \_ \_ hashprop- \_ ID

Eine Liste der derzeit definierten erweiterten Zertifikat Eigenschaften und Beschreibungen der Bedeutung und Verwendung der einzelnen Eigenschaften finden Sie unter [**certgetcertifiaseecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) und [**certsetcertifikatecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Certgetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**Certgetctlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**Certsetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**Certsetctlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
