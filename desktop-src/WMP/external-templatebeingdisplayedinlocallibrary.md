---
title: Extern. templatebingdisplayedinlocallibrary
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. templatebingdisplayedinlocallibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Externe. templatebingdisplayedinlocallibrary-Fenster Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369722"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>Extern. templatebingdisplayedinlocallibrary

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **templatebeingdisplayedinlocallibrary** -Eigenschaft gibt an, ob der von der aktuellen Ermittlungs Seite dargestellte Feed im Strukturansicht-Steuerelement der lokalen Bibliothek angezeigt wird.

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Schreib geschützter **boolescher** Wert. **True** gibt an, dass der Feed im Strukturansicht-Steuerelement der lokalen Bibliothek angezeigt wird.

## <a name="remarks"></a>Bemerkungen

Eine Ermittlungs Seite, die einen Feed für eine dynamische Wiedergabeliste darstellt, kann eine Schaltfläche anzeigen, mit der der Benutzer den Feed in seiner lokalen Bibliothek speichern kann. Das Speichern des Feeds bedeutet in diesem Kontext, dass einige Metadaten auf dem Computer des Benutzers gespeichert werden, und der Feed wird unter dem Knoten " **Playlists** " im Strukturansicht-Steuerelement der lokalen Bibliothek aufgelistet. Das Skript auf der Ermittlungs Seite kann die Eigenschaft **templatebeingdisplayedinlocallibrary** überprüfen, um zu bestimmen, ob der Benutzer den Feed bereits in der lokalen Bibliothek gespeichert hat. Wenn der Benutzer den Feed bereits gespeichert hat, sollte auf der Ermittlungs Seite die Schaltfläche Speichern nicht angezeigt werden.

Eine Suchseite, die einen Radio Feed darstellt, sollte die Eigenschaft **templatebeingdisplayedinlocallibrary** aus demselben Grund überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





