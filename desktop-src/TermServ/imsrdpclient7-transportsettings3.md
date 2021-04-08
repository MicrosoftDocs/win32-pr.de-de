---
title: IMsRdpClient7 TransportSettings3-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientTransportSettings3-Schnittstelle unterstützt.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- TransportSettings3-Eigenschaft Remotedesktopdienste
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
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
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740561"
---
# <a name="imsrdpclient7transportsettings3-property"></a>IMsRdpClient7:: TransportSettings3-Eigenschaft

Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstelle unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Adresse eines [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstellen Zeigers, der das-Objekt empfängt.

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

 

 





