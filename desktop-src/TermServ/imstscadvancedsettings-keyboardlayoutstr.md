---
title: Imstscadvancedsettings keyboardlayoutstr-Eigenschaft
description: Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Keyboardlayoutstr-Eigenschaft Remotedesktopdienste
- Keyboardlayoutstr-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, keyboardlayoutstr-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741504"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Imstscadvancedsettings:: keyboardlayoutstr-Eigenschaft

Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.

Wenn diese Eigenschaft nicht festgelegt ist, verwendet das Steuerelement das Standardlayout, das von der [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) -Funktion zurückgegeben wird.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des aktiven Eingabe Gebiets Schema Bezeichners.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Die-Eigenschaft ist eine hexadezimale Zahl mit acht Ziffern in Form einer Zeichenfolge. Die unteren vier Ziffern stellen den sprach Bezeichner dar, und die oberen vier Ziffern stellen die Tastatur Variation innerhalb dieser Sprache dar. Beispielsweise würde "00000409" die Standardtastatur von US-Englisch darstellen, da "0409" der US-englische sprach Bezeichner ist. Die Dvorak-Variation der US-englischen Tastatur hat den Bezeichner "00010409". Sie finden die verfügbaren Tastaturlayouts, die nach Ihren Tastaturlayout-bezeichlern aufgeführt sind, in der Registrierung unter

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

