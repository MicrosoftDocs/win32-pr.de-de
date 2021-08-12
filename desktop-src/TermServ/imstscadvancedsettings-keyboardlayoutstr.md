---
title: IMsTscAdvancedSettings KeyBoardLayoutStr -Eigenschaft
description: Gibt den Namen des aktiven Eingabe-Locale Identifiers an (früher als Tastaturlayout bezeichnet), der für die Verbindung verwendet werden soll.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- KeyBoardLayoutStr-Remotedesktopdienste
- KeyBoardLayoutStr-Eigenschaft Remotedesktopdienste , IMsTscAdvancedSettings-Schnittstelle
- IMsTscAdvancedSettings-Schnittstelle Remotedesktopdienste , KeyBoardLayoutStr-Eigenschaft
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
ms.openlocfilehash: 3c87cb55b22658f704b328a51435ca2554d4c6574e25484253f9899475918642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606177"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>IMsTscAdvancedSettings::KeyBoardLayoutStr -Eigenschaft

Gibt den Namen des aktiven Eingabe-Locale Identifiers an (früher als Tastaturlayout bezeichnet), der für die Verbindung verwendet werden soll.

Wenn diese Eigenschaft nicht festgelegt ist, verwendet das Steuerelement das Standardlayout, das von der [**GetKeyboardLayout-Funktion zurückgegeben**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) wird.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des aktiven Eingabe-Locale Identifiers.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Die -Eigenschaft ist eine achtstellige Hexadezimalzahl in Zeichenfolgenform. Die unteren vier Ziffern stellen den Sprachbezeichner dar, und die oberen vier Ziffern stellen die Tastaturvariation innerhalb dieser Sprache dar. Beispielsweise würde "00000409" die Standardtastatur für englisch (USA) darstellen, da "0409" der Bezeichner der englischen Sprache in den USA ist. Die Dvorak-Variante der us-amerikanischen Englischtastatur hat den Bezeichner "00010409". Sie finden die verfügbaren Tastaturlayouts, die nach ihren Tastaturlayoutbezeichnern aufgeführt sind, in der Registrierung unter .

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings ist als 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

