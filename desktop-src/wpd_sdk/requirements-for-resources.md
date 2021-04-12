---
description: Anforderungen für Ressourcen
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Anforderungen für Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217189"
---
# <a name="requirements-for-resources"></a>Anforderungen für Ressourcen

Tragbare Windows-Geräte definieren die folgenden Ressourcen Kategorien als **PropertyKey** -Werte. Diese Werte werden verwendet, um einzelne Ressourcen in einem-Objekt zu beschreiben. Der *PID* -Member des Eigenschafts Schlüssels kann sich unterscheiden, um unterschiedliche Ressourcen desselben Typs für alle Typen außer dem Standardwert der **WPD- \_ Ressource \_** zu beschreiben, der nur eine Ressource beschreiben kann. Die Seite verknüpfte Beschreibung für jeden Ressourcentyp listet die Attribute auf, die von dieser Ressource unterstützt werden.



| Ressourcenpropertykey                                                | BESCHREIBUNG                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)              | Gibt die gesamte Datei hinter dem Objekt an. Dies ist die einzige erforderliche Ressource für ein beliebiges Objekt mit einer Ressource. |
| [**WPD- \_ Ressourcen \_ Album- \_ Grafik**](wpd-resource-album-art.md)         | Gibt ein Bild an, das die Albumgrafik für das-Objekt darstellt.                                           |
| [**WPD \_ \_ - \_ ressourcenaudioclip**](wpd-resource-audio-clip.md)       | Gibt einen Audioclip für das-Objekt an.                                                                        |
| [**WPD- \_ Ressourcen \_ Kontakt \_ Foto**](wpd-resource-contact-photo.md) | Gibt ein Bild an, das ein Foto der Person darstellt, auf die im Contact-Objekt verwiesen wird.                |
| [**WPD- \_ Ressource \_ generisch**](wpd-resource-generic.md)              | Eine generische Ressource des nicht definierten Datentyps. Dies sollte als Bytearray behandelt werden.                             |
| [**Symbol für WPD- \_ Ressource \_**](wpd-resource-icon.md)                    | Symbol                                                                                                       |
| [**WPD- \_ Ressourcen \_ Miniaturansicht**](wpd-resource-thumbnail.md)          | Ein Miniaturbild.                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



