---
title: Imsrdpclientadvancedsettings-hotkeyctrlaltdel-Eigenschaft
description: Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + ENTF, auch als "sichere Aufmerksamkeit" (Secure Attention Sequence, SAS) bezeichnet.
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391603"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a>Imsrdpclientadvancedsettings:: hotkeyctrlaltdel-Eigenschaft

Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + ENTF, auch als "sichere Aufmerksamkeit" (Secure Attention Sequence, SAS) bezeichnet.

> [!Note]  
> STRG + ALT + ENTF wird nie an den Remote Server umgeleitet, auch wenn die [keyboardhuokmode](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft aktiviert ist. STRG + ALT + ENTF ist die lokale SAS-Sequenz.

 

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Code des virtuellen Schlüssels. **VK \_ "End** " ist die Standardeinstellung.

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

 

 





