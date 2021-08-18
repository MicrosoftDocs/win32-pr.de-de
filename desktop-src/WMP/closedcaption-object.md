---
title: ClosedCaption-Objekt
description: Das ClosedCaption-Objekt bietet eine Möglichkeit, Untertitel in einen Medienclip einzuschließen. Der Beschriftungstext befindet sich in einer SAMI-Datei (Synchronized Accessible Media Interchange).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- ClosedCaption-Objekt Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10ae51af31e724bd066dbbb9e826569da40159460eb1e7bf570aea331dff86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119594"
---
# <a name="closedcaption-object"></a>ClosedCaption-Objekt

Das **ClosedCaption-Objekt** bietet eine Möglichkeit, Untertitel in einen Medienclip einzuschließen. Der Beschriftungstext befindet sich in einer SAMI-Datei (Synchronized Accessible Media Interchange).

Das **ClosedCaption-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | Beschreibung                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Gibt den Namen des Frames oder Steuerelements an, der die Beschriftung anzeigt, oder ruft den Namen ab.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Gibt den Namen der Datei an, die die für Untertitel benötigten Informationen enthält, oder ruft sie ab. |
| [SAMILang](closedcaption-samilang.md)             | Gibt die Sprache an, die für Untertitel angezeigt wird, oder ruft sie ab.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Ruft die Anzahl der Sprachen ab, die von der aktuellen SAMI-Datei unterstützt werden.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Gibt den Untertitelstil an oder ruft sie ab.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Ruft die Anzahl von Formatvorlagen ab, die von der aktuellen SAMI-Datei unterstützt werden.                                   |



 

Das **ClosedCaption-Objekt** unterstützt die folgenden Methoden.



| Methode                                                 | Beschreibung                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Ruft den Gebietsschemabezeichner (LCID) einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Ruft den Namen einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Ruft den Namen eines Stils ab, der von der aktuellen SAMI-Datei unterstützt wird.                        |



 

Auf **das ClosedCaption-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                                  |
|-----------------------------|-------------------------------------------|
| [Player](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




