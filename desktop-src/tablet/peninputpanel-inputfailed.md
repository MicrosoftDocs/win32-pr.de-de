---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt "pinputpanel" Benutzereingaben in das angefügte Steuerelement einfügen konnte.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Das Ereignis "pinputpanel. InputFailed" (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352775"
---
# <a name="peninputpanelinputfailed-event"></a>"Pinputpanel. InputFailed"-Ereignis

Veraltet. Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.

Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt " [**pinputpanel**](peninputpanel-class.md) " Benutzereingaben in das angefügte Steuerelement einfügen konnte.

## <a name="syntax"></a>Syntax


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Das Fenster Handle des Steuer Elements [**, das das Objekt "**](peninputpanel-class.md) " mit dem Objekt "-Objekt" aufgerufen hat.

</dd> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der virtuelle Schlüssel, der dem gedrückten Schlüssel entspricht.

</dd> <dt>

*Text* \[ in\]
</dt> <dd>

Die Zeichenfolge, die in das Steuerelement eingefügt werden soll, das durch den *HWND* -Parameter dargestellt wird, als das **InputFailed** -Ereignis ausgelöst wurde.

Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ in\]
</dt> <dd>

Der Zustand der Tastatur modifiziererer, einschließlich Shift, Caps, STRG und alt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das **InputFailed** -Ereignis tritt auf, wenn sich der Eingabefokus ändert, bevor Benutzereingaben in das angefügte Steuerelement eingefügt wurden. Wenn der Benutzer z. b. Freihand in den Schreib-Pad eingibt und dann auf ein anderes Bearbeitungs Steuerelement tippt, bevor die Erkennung abgeschlossen werden konnte, wird dieses Ereignis ausgelöst.

Wenn Sie das Fenster Handle verwenden, das an dieses Ereignis übermittelt wurde, können Sie den Text selbst einfügen, wenn dieses Ereignis auftritt.

> [!Note]  
> Ab Microsoft Windows XP Tablet PC Edition 2005 gilt das Ereignis " **InputFailed** " nicht mehr. Text wird immer eingefügt, bevor der Fokus geändert wird.

 

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

 

 




