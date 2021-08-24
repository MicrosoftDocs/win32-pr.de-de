---
description: Gibt einen Ressourcentyp an, der nicht anderweitig von portablen Windows definiert wird.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c418299474373d8b960d15c429ea98d887cc404be49c8d38c7d2bb83611c4ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805870"
---
# <a name="wpd_resource_generic"></a>WPD \_ RESOURCE \_ GENERIC

Gibt einen Ressourcentyp an, der nicht anderweitig von portablen Windows definiert wird. Sie können eigene benutzerdefinierte Ressourcen definieren, die benutzerdefinierte oder Windows portable Geräte definierte Attribute unterstützen. Jede Ressource, die Sie erstellen, muss jedoch die folgenden Attribute unterstützen.



| Attributname                                                                                                            | Erforderlich oder optional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ \_ GESAMTGRÖßE](resource-attribute-properties.md)              | Erforderlich.                                              |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN \_ LESEN](attributes.md)                                     | Erforderlich, wenn Clients diese Ressource lesen können.            |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN \_ SCHREIBEN](attributes.md)                                   | Erforderlich, wenn Clients in diese Ressource schreiben können.        |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN LÖSCHEN \_](attributes.md)                                 | Erforderlich, wenn Clients diese Ressource löschen können.          |
| [WPD \_ RESOURCE \_ ATTRIBUTE \_ OPTIMAL \_ READ \_ BUFFER \_ SIZE](attributes.md)   | Erforderlich, wenn Clients Über Lesezugriff auf die Ressource haben.  |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ OPTIMALE \_ \_ \_ SCHREIBPUFFERGRÖßE](attributes.md) | Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben. |
| [\_ \_ WPD-RESSOURCENATTRIBUTFORMAT \_](resource-attribute-properties.md)                       | Erforderlich.                                              |
| [RESSOURCENSCHLÜSSEL DES \_ \_ WPD-RESSOURCENATTRIBUTS \_ \_](resource-attribute-properties.md)                                              | Empfohlen.                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anforderungen für Ressourcen**](requirements-for-resources.md)
</dt> </dl>

 

 



