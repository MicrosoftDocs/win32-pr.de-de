---
title: IMsRdpClient4 AdvancedSettings5 (Eigenschaft)
description: Ruft einen Zeiger auf eine IMsRdpClientAdvancedSettings4-Schnittstelle ab.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- AdvancedSettings5-Remotedesktopdienste
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaft Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , AdvancedSettings5-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb8efd8fae25be768a1b758389b5ca7c20a9f3f8b414e62acb865fecf83eeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138953"
---
# <a name="imsrdpclient4advancedsettings5-property"></a>IMsRdpClient4::AdvancedSettings5 (Eigenschaft)

Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4-Schnittstelle**](imsrdpclientadvancedsettings4.md) ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf die [**IMsRdpClientAdvancedSettings4-Schnittstelle.**](imsrdpclientadvancedsettings4.md) Die -Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Clientsteuersystem zu festlegen.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, **wird S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient4 ist als 095E0738-D97D-488b-B9F6-DD0E8D66C0DE definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





