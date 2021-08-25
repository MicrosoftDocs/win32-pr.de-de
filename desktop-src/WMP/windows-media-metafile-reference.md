---
title: Windows Referenz zur Medienmetadatei
description: Windows Referenz zur Medienmetadatei
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Medienmetadateien,Referenz
- metafiles,reference
- Referenz für Windows Medienmetadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b00cd604ec94c42ef90f08a8875edb4fda92ba8267c7e4a7d7b5505c2fb57932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862260"
---
# <a name="windows-media-metafile-reference"></a>Windows Referenz zur Medienmetadatei

In dieser Referenz werden Elemente und Dateinamenerweiterungen für Windows Medienmetadateien dokumentiert. Der Verweis ist in die folgenden Abschnitte unterteilt.



| `Section`                                                                                    | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Referenz zu Medienmetadateielementen](windows-media-metafile-elements-reference.md) | Dokumentiert Metadateielemente, einschließlich Definitionen, Attribute und deren Werte sowie spezielle Bedingungen im Zusammenhang mit den einzelnen Elementen. |
| [Dateinamenerweiterungen](file-name-extensions.md)                                           | Dokumentiert Dateinamenerweiterungen für Metadateien mit Regeln und Richtlinien für deren Verwendung.                                                  |



 

Windows Medienmetadateien sind Textdateien, die Informationen zu einem Dateistream und seiner Darstellung bereitstellen. Die Metadateien basieren auf der Extensible Markup Language(XML)-Syntax und werden aus verschiedenen XML-ähnlichen Elementen mit ihren Tags und Attributen erstellt. Jedes Element definiert eine Einstellung oder Aktion für Streamingmedien.

Für Metadateien sind zwei Sätze von Elementtags verfügbar. Clientseitige Metadateien verfügen über einen Satz von Elementen, und serverseitige Metadateien haben einen anderen Satz von Elementen.

Wenn ein Elementtag keine untergeordneten Elemente enthält (elemente, die ändern oder in einem anderen Element enthalten sind), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags statt eines schließenden Tags verwendet werden. Wenn untergeordnete Elemente nicht zwischen dem öffnenden und dem schließenden Tag für ein Element angezeigt werden, sind sie keine untergeordneten Elemente für dieses Element und werden ignoriert oder verursachen einen Fehler in der Syntax der Metadatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen Windows Medienmetadateien**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Medienmetadateien**](windows-media-metafiles.md)
</dt> </dl>

 

 




