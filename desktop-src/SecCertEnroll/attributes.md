---
description: 'Attribute (Zertifikatregistrierungs-API): Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer Zertifizierungsstelle zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.'
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
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118428"
---
# <a name="attributes-certificate-enrollment-api"></a>Attribute (Zertifikatregistrierungs-API)

Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer Zertifizierungsstelle zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann. Jedes Attribut ist eine [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER)-codierte ASN.1-Struktur [*(Abstract Syntax Notation One),*](/windows/desktop/SecGloss/a-gly) die einen Objektbezeichner (Object Identifier, OID) und 0 (null) oder mehr Werte enthält. Attribute werden mithilfe von Schnittstellen definiert, die in der Zertifikatregistrierungs-API enthalten sind. In den folgenden Themen werden Attribute ausführlicher erläutert:

-   [Unterstützte Attribute](supported-attributes.md)
-   [Attributarchitektur](attribute-architecture.md)
-   [PKCS \# 7-Attribute](pkcs--7-attributes.md)
-   [PKCS \# 10-Attribute](pkcs--10-attributes.md)
-   [CMC-Attribute](cmc-attributes.md)

 

 
