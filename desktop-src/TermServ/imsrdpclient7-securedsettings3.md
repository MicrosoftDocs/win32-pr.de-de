---
title: IMsRdpClient7 SecuredSettings3 (Eigenschaft)
description: Ruft ein Objekt ab, das die IMsRdpClientSecuredSettings2-Schnittstelle unterstützt.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- SecuredSettings3-Remotedesktopdienste
- SecuredSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaft Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , SecuredSettings3-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bcdaae672ca59c65bea46d97a34046c7e48c6f0964c1a5b97cdcef77c14ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737170"
---
# <a name="imsrdpclient7securedsettings3-property"></a>IMsRdpClient7::SecuredSettings3 (Eigenschaft)

Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2-Schnittstelle**](imsrdpclientsecuredsettings2.md) unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Adresse eines [**IMsRdpClientSecuredSettings2-Schnittstellenzeigers,**](imsrdpclientsecuredsettings2.md) der das -Objekt empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





