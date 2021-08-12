---
title: IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseLeft (Eigenschaft)
description: Gibt den virtuellen Tastencode an, der STRG+ALT hinzugefügt werden soll, um den Hotkey-Ersatz für STRG+ALT+NACH-LINKS-TASTE zu bestimmen.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- HotKeyFocusReleaseLeft-Remotedesktopdienste
- HotKeyFocusReleaseLeft-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , HotKeyFocusReleaseLeft-Eigenschaft
- HotKeyFocusReleaseLeft-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , HotKeyFocusReleaseLeft-Eigenschaft
- HotKeyFocusReleaseLeft-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , HotKeyFocusReleaseLeft-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a5df8cd9c85ecccaf2de32a0e82ac604429f7b9f1e4801e3bfb025de8116d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607905"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a>IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft (Eigenschaft)

Gibt den virtuellen Tastencode an, der STRG+ALT hinzugefügt werden soll, um den Hotkey-Ersatz für STRG+ALT+NACH-LINKS-TASTE zu bestimmen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Virtuelle Schlüsselcode.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur von Remotedesktopverbindung 6.1- und 7.0-Clients unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





