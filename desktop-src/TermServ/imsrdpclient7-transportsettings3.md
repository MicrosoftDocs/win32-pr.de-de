---
title: IMsRdpClient7 TransportSettings3-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientTransportSettings3-Schnittstelle unterstützt.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- TransportSettings3-Eigenschaft Remotedesktopdienste
- TransportSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , TransportSettings3-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff2c3d3427c9c8c5323f3c4cbea9d194c81d223c2a07ee364f87dd1dd2c33d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033340"
---
# <a name="imsrdpclient7transportsettings3-property"></a>IMsRdpClient7::TransportSettings3-Eigenschaft

Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3-Schnittstelle**](imsrdpclienttransportsettings3.md) unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Adresse eines [**IMsRdpClientTransportSettings3-Schnittstellenzeigers,**](imsrdpclienttransportsettings3.md) der das Objekt empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





