---
title: External.saveCurrentViewToLibrary-Methode
description: Die saveCurrentViewToLibrary-Methode erstellt eine Wiedergabeliste aus den Medienelementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- saveCurrentViewToLibrary-Windows Media Player
- saveCurrentViewToLibrary-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , saveCurrentViewToLibrary-Methode
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
ms.openlocfilehash: cf14a6f712a72116860e7251edae73c91c4ef1dfb70876fd5f80dc329591673a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648440"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>External.saveCurrentViewToLibrary-Methode

Die **saveCurrentViewToLibrary-Methode** erstellt eine Wiedergabeliste aus den Medienelementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.

## <a name="syntax"></a>Syntax


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyListName* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die einen Benutzerfreundlichen Namen für die Wiedergabeliste angibt. Windows Media Player zeigt diesen Namen auf der Benutzeroberfläche an.

</dd> <dt>

*Lokal* \[ In\]
</dt> <dd>

**Boolescher Wert,** der angibt, ob die Wiedergabeliste dynamisch oder statisch ist. **TRUE** gibt dynamisch an, **und FALSE** gibt static an.

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

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





