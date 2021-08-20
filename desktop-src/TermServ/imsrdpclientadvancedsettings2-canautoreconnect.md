---
title: IMsRdpClientAdvancedSettings2 CanAutoReconnect (Eigenschaft)
description: Gibt an, ob das Clientsteuer steuerelement im Falle einer Trennung der Netzwerkverbindung automatisch wieder eine Verbindung mit der aktuellen Sitzung herstellen kann.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- CanAutoReconnect-Remotedesktopdienste
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
- CanAutoReconnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , CanAutoReconnect-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d64ac732af45e935ddef8d0436bc2b9173854394c55bcc19c085dec5926e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001418"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a>IMsRdpClientAdvancedSettings2::CanAutoReconnect (Eigenschaft)

Gibt an, ob das Clientsteuer steuerelement im Falle einer Trennung der Netzwerkverbindung automatisch wieder eine Verbindung mit der aktuellen Sitzung herstellen kann.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt **VARIANT \_ TRUE,** wenn das Steuerelement die Verbindung automatisch wiederherstellen kann, andernfalls **VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Zu situationen, in denen die automatische wiederhergestellte Verbindung möglicherweise nicht aktiviert ist, gehören dieJenigen, in denen ein Administrator die Gruppenrichtlinie verwendet, um die automatische Verbindung zu deaktivieren, und Ältere Umgebungen, die die automatische Wiederherstellung der Verbindung nicht unterstützen.

Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

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

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





