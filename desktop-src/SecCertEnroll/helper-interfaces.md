---
description: Die folgenden allgemeinen Verwendungsschnittstellen werden von der Zertifikatregistrierungs-API unterstützt.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Hilfsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec54f9e092bb7675f18a28e7af8599a4e870b5aec1d88d0c5d3332c33c2bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779539"
---
# <a name="helper-interfaces"></a>Hilfsschnittstellen

Die folgenden allgemeinen Verwendungsschnittstellen werden von der Zertifikatregistrierungs-API unterstützt.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | Erstellt eine Unicode-codierte Zeichenfolge aus einem Bytearray, erstellt ein Bytearray aus einer Unicode-codierten Zeichenfolge und ändert den Typ der Unicode-Codierung, die auf eine Zeichenfolge angewendet wird. |
| [**ICertificateAttestationChallenge**](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | Unterstützt Herausforderungen beim Zertifikatnachweis.                                                                                                                           |
| [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | Stellt einen Objektbezeichner dar.                                                                                                                                       |
| [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | Verwaltet eine Auflistung von [**IObjectId-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                                                                                        |
| [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | Stellt einen X.500-Distinguished Name dar.                                                                                                                                |
| [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | X.509 Endorsement Key-Schnittstelle                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



