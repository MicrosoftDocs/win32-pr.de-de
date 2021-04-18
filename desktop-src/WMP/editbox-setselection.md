---
title: EditBox. setSelection
description: Die setSelection-Methode wählt den Text im Bearbeitungsfeld-Steuerelement vom angegebenen Start Index bis zum angegebenen endIndex aus.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- EditBox. setSelection-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364853"
---
# <a name="editboxsetselection"></a>EditBox. setSelection

Die **setSelection** -Methode wählt den Text im Bearbeitungsfeld-Steuerelement vom angegebenen Start Index bis zum angegebenen endIndex aus.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="start"></span><span id="START"></span>*begonnen*
</dt> <dd>

**Number** (**Long**), die den Zeichen Index der Anfangsposition des ausgewählten Texts enthält.

</dd> <dt>

<span id="end"></span><span id="END"></span>*Schließlich*
</dt> <dd>

**Number** (**Long**), die den Zeichen Index der Endposition des ausgewählten Texts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Start Wert 0 und das Ende 1 ist, wird der gesamte Text im Bearbeitungsfeld-Steuerelement ausgewählt. Wenn der Start Wert 1 ist, wird jede aktuelle Auswahl deaktiviert.

Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EditBox. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EditBox. ReplaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





