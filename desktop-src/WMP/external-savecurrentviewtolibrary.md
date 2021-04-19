---
title: Extern. savecurrentviewylibrary-Methode
description: Die savecurrentviewylibrary-Methode erstellt eine Wiedergabeliste aus den Medien Elementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- savecurrentviewylibrary-Methode, Windows Media Player
- savecurrentviewylibrary-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, savecurrentviewylibrary-Methode
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369545"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>Extern. savecurrentviewylibrary-Methode

Die **savecurrentviewylibrary** -Methode erstellt eine Wiedergabeliste aus den Medien Elementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.

## <a name="syntax"></a>Syntax


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Friendlylistname* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die einen anzeigen Amen für die Wiedergabeliste angibt. In Windows Media Player wird dieser Name in der Benutzeroberfläche angezeigt.

</dd> <dt>

*Lokal* \[ in\]
</dt> <dd>

**Boolescher** Wert, der angibt, ob die Wiedergabeliste dynamisch oder statisch ist. **True** gibt Dynamic an, und **false** gibt Static an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





