---
description: Gibt die gesamte Datei hinter dem Objekt an. Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich derjenigen, die nicht von anderen mobilen Windows-Geräten (z. b. einem benutzerdefinierten Objekttyp) abgedeckt werden.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529891"
---
# <a name="wpd_resource_default"></a>WPD- \_ Ressourcen \_ Standard

Gibt die gesamte Datei hinter dem Objekt an. Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich derjenigen, die nicht von anderen mobilen Windows-Geräten (z. b. einem benutzerdefinierten Objekttyp) abgedeckt werden.

Alle Ressourcen, die in die angegebene Ressource eingebettet sind, werden eingeschlossen. Beispielsweise kann die Standardressource eines Stamm Ordners von Kontakten alle in der Liste eingefügten Kontakte enthalten. Allerdings werden alle untergeordneten Ressourcen, die nur durch Metadaten oder Verweise *verknüpft* sind, nicht eingeschlossen. Ein Beispiel hierfür wäre eine Wiedergabeliste, die nur über Metadatenverweise oder Textpfad-Verweise in der Datei mit Audiodateien verknüpft werden kann.

Der einzige zulässige *PID* -Wert für diesen **PropertyKey** ist 0 (null).

Dieser Ressourcentyp muss die folgenden Attribute unterstützen.



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

 

 



