---
description: Gibt einen Ressourcentyp an, der nicht anderweitig von tragbaren Windows-Geräten definiert wird.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128948"
---
# <a name="wpd_resource_generic"></a>WPD- \_ Ressource \_ generisch

Gibt einen Ressourcentyp an, der nicht anderweitig von tragbaren Windows-Geräten definiert wird. Sie können eigene benutzerdefinierte Ressourcen definieren, die beliebige benutzerdefinierte oder von Windows Portable Geräte definierte Attribute unterstützen. Jede Ressource, die Sie erstellen, muss jedoch die folgenden Attribute unterstützen.



| Attributname                                                                                                            | Erforderlich oder optional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_](resource-attribute-properties.md)              | Erforderlich.                                              |
| [WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen](attributes.md)                                     | Erforderlich, wenn diese Ressource von Clients gelesen werden kann.            |
| [WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben](attributes.md)                                   | Erforderlich, wenn Clients in diese Ressource schreiben können.        |
| [Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.](attributes.md)                                 | Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.          |
| [WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe](attributes.md)   | Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.  |
| [Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_](attributes.md) | Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben. |
| [WPD- \_ Ressourcen \_ Attribut \_ Format](resource-attribute-properties.md)                       | Erforderlich.                                              |
| [Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_](resource-attribute-properties.md)                                              | Empfohlen.                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anforderungen für Ressourcen**](requirements-for-resources.md)
</dt> </dl>

 

 



