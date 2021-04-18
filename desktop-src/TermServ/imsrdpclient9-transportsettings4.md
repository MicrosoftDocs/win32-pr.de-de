---
title: IMsRdpClient9 TransportSettings4-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientTransportSettings4-Schnittstelle unterstützt.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- TransportSettings4-Eigenschaft Remotedesktopdienste
- TransportSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings4-Eigenschaft
- TransportSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings4-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340378"
---
# <a name="imsrdpclient9transportsettings4-property"></a>IMsRdpClient9:: TransportSettings4-Eigenschaft

Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstelle unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt einen [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstellen Zeiger zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





