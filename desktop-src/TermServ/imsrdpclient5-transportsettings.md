---
title: IMsRdpClient5 TransportSettings (Eigenschaft)
description: Ruft ab, was durch ein Skript an die imsrdpclienttransportsettings-Schnittstelle übermittelt wurde.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103163"
---
# <a name="imsrdpclient5transportsettings-property"></a>IMsRdpClient5:: TransportSettings (Eigenschaft)

Ruft ab, was durch ein Skript an die [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstelle übermittelt wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstellen Zeiger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

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

 

 





