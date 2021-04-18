---
title: Media. AttributeCount
description: Die AttributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. AttributeCount-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368691"
---
# <a name="mediaattributecount"></a>Media. AttributeCount

Die **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **AttributeCount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **AttributeCount** , um die Anzahl der Attribute zu bestimmen, die im aktuellen Medien Element verfügbar sind. Der Code verwendet diesen Wert, um eine Liste der Attributnamen und-Werte in einem HTML-Textbereich mit dem Namen MyText auszugeben. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





