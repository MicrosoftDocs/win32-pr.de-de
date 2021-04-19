---
title: Imsrdpclientadvancedsettings-hotkeyctrlesc (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der alt hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ESC zu bestimmen.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyctrlesc-Eigenschaft
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339965"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a>Imsrdpclientadvancedsettings:: hotkeyctrlesc (Eigenschaft)

Gibt den Code des virtuellen Schlüssels an, der alt hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ESC zu bestimmen.

Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Code des virtuellen Schlüssels. **VK \_ Home** ist der Standardwert, wobei Alt + Home als resultierende Sequenz angezeigt wird.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





