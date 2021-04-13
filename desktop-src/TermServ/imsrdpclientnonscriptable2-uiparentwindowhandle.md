---
title: IMsRdpClientNonScriptable2 uianentwindowhandle-Eigenschaft
description: Legt das Fenster Handle fest, das das übergeordnete Fenster für alle Dialogfelder ist, die vom Steuerelement angezeigt werden, oder ruft es ab. Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475225"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a>IMsRdpClientNonScriptable2:: uianentwindowhandle-Eigenschaft

Legt das Fenster Handle fest, das das übergeordnete Fenster für alle Dialogfelder ist, die vom Steuerelement angezeigt werden, oder ruft es ab. Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a>Eigenschaftswert

Das neue Fenster handle.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 ist als 17a5e535-4072-4fa4-af32-c8d0d47345e9 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Onauthenticationwarningangezeigte**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**Onauthenticationwarningverworfen**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





