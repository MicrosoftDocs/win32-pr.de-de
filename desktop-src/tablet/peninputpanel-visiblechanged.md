---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn das ""-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: "\"Pinputpanel. VisibleChanged\"-Ereignis (msink AUT. h)"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362992"
---
# <a name="peninputpanelvisiblechanged-event"></a>"Pinputpanel. VisibleChanged"-Ereignis

Veraltet. Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.

Tritt auf, [**Wenn das "**](peninputpanel-class.md) "-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Neusicht barkeit* \[ in\]
</dt> <dd>

**Variant \_ TRUE** , wenn das Objekt " [**pinputpanel**](peninputpanel-class.md) " sichtbar wird. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das **VisibleChanged** -Ereignis gilt für den Tablet PC-Eingabe Panel-Hover-Ziel. Sie wird jedoch nicht ausgelöst, wenn das Hover-Ziel erweitert wird, um den vollständigen Tablet PC-Eingabebereich anzuzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Pendel Panel"**](peninputpanel-class.md)
</dt> </dl>

 

 




