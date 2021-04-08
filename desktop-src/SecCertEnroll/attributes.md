---
description: Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine Zertifizierungsstelle (Certification Authority, ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attribute (Zertifikatregistrierungs-API)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753481"
---
# <a name="attributes-certificate-enrollment-api"></a>Attribute (Zertifikatregistrierungs-API)

Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine Zertifizierungsstelle (Certification Authority, ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann. Jedes Attribut ist eine [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) codierte [*abstrakte Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1)-Struktur, die einen Objekt Bezeichner (OID) und NULL oder mehr Werte enthält. Attribute werden mithilfe von Schnittstellen definiert, die in der Zertifikatregistrierungs-API enthalten sind. In den folgenden Themen werden Attribute ausführlicher erläutert:

-   [Unterstützte Attribute](supported-attributes.md)
-   [Attribut Architektur](attribute-architecture.md)
-   [PKCS \# 7-Attribute](pkcs--7-attributes.md)
-   [PKCS \# 10-Attribute](pkcs--10-attributes.md)
-   [CMC-Attribute](cmc-attributes.md)

 

 
