---
description: Anforderungen für Ressourcen
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Anforderungen für Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca302fcd11abf4bbadc1adfafb1a1be67141055ea7f9a5366991f231cca44fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027147"
---
# <a name="requirements-for-resources"></a>Anforderungen für Ressourcen

Windows Portable Geräte definieren die folgenden Ressourcenkategorien als **PROPERTYKEY-Werte.** Diese Werte werden verwendet, um einzelne Ressourcen in einem Objekt zu beschreiben. Der *Pid-Member* des Eigenschaftsschlüssels kann sich unterscheiden, um verschiedene Ressourcen desselben Typs für alle Typen mit Ausnahme von **WPD \_ RESOURCE \_ DEFAULT** zu beschreiben, die nur eine Ressource beschreiben können. Auf der verknüpften Beschreibungsseite für jeden Ressourcentyp werden die von dieser Ressource unterstützten Attribute aufgelistet.



| Resource PROPERTYKEY                                                | Beschreibung                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md)              | Gibt die gesamte Datei hinter dem -Objekt an. Dies ist die einzige erforderliche Ressource für jedes Objekt mit einer Ressource. |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md)         | Gibt ein Bild an, das die Albumgrafik für das -Objekt darstellt.                                           |
| [**WPD \_ RESOURCE \_ AUDIO \_ CLIP**](wpd-resource-audio-clip.md)       | Gibt einen Audioclip für das -Objekt an.                                                                        |
| [**WPD \_ RESOURCE \_ CONTACT \_ PHOTO**](wpd-resource-contact-photo.md) | Gibt ein Bild an, das ein Foto der Person darstellt, auf die im Kontaktobjekt verwiesen wird.                |
| [**\_WPD-RESSOURCE \_ GENERISCH**](wpd-resource-generic.md)              | Eine generische Ressource des nicht definierten Datentyps. Dies sollte als Bytearray behandelt werden.                             |
| [**\_WPD-RESSOURCENSYMBOL \_**](wpd-resource-icon.md)                    | Symbol                                                                                                       |
| [**\_ \_ WPD-RESSOURCENMINIATURANSICHT**](wpd-resource-thumbnail.md)          | Ein Miniaturbild.                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



