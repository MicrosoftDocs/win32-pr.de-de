---
description: Gibt die gesamte Datei hinter dem -Objekt an. Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich der ressourcentypen, die nicht von anderen Windows Portable Devices-Ressourcentypen abgedeckt werden, z. B. einem benutzerdefinierten Objekttyp.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d939cf58033baded231363b39410c2e527fe303075c94255a00ba96831a609b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805880"
---
# <a name="wpd_resource_default"></a>\_WPD-RESSOURCENSTANDARD \_

Gibt die gesamte Datei hinter dem -Objekt an. Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich der ressourcentypen, die nicht von anderen Windows Portable Devices-Ressourcentypen abgedeckt werden, z. B. einem benutzerdefinierten Objekttyp.

Alle Ressourcen, die in die angegebene Ressource eingebettet sind, werden eingeschlossen. Beispielsweise kann die Standardressource eines Stammordners von Kontakten alle geschachtelten Kontakte enthalten. Untergeordnete Ressourcen, die lediglich durch Metadaten oder Verweise *verknüpft* sind, sind jedoch nicht enthalten. Ein Beispiel hierfür wäre eine Wiedergabeliste, die nur über Metadatenverweise oder Textpfadverweise in der Datei mit Audiodateien verknüpft werden kann.

Der einzige zulässige *Pid-Wert* für diesen **PROPERTYKEY** ist 0 (null).

Dieser Ressourcentyp muss die folgenden Attribute unterstützen.



| Attributname                                                                                                            | Erforderlich oder optional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_GESAMTGRÖßE DES WPD-RESSOURCENATTRIBUTS \_ \_ \_](resource-attribute-properties.md)              | Erforderlich.                                              |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELESEN \_ WERDEN](attributes.md)                                     | Erforderlich, wenn Clients diese Ressource lesen können.            |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN \_ SCHREIBEN](attributes.md)                                   | Erforderlich, wenn Clients in diese Ressource schreiben können.        |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELÖSCHT \_ WERDEN](attributes.md)                                 | Erforderlich, wenn Clients diese Ressource löschen können.          |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ OPTIMALE \_ \_ \_ LESEPUFFERGRÖßE](attributes.md)   | Erforderlich, wenn Clients Lesezugriff auf die Ressource haben.  |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ OPTIMALE \_ \_ \_ SCHREIBPUFFERGRÖßE](attributes.md) | Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben. |
| [\_ \_ WPD-RESSOURCENATTRIBUTFORMAT \_](resource-attribute-properties.md)                       | Erforderlich.                                              |
| [RESSOURCENSCHLÜSSEL DES \_ WPD-RESSOURCENATTRIBUTS \_ \_ \_](resource-attribute-properties.md)                                              | Empfohlen.                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anforderungen für Ressourcen**](requirements-for-resources.md)
</dt> </dl>

 

 



