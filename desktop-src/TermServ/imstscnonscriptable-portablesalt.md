---
title: IMsTscNonScriptable PortableSalt-Eigenschaft
description: Diese Eigenschaft wird nicht mehr unterstützt.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- PortableSalt-Eigenschaft Remotedesktopdienste
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsTscNonScriptable-Schnittstelle
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , MsTscAx-Objekt
- MsTscAx-Objekt Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
- PortableSalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , PortableSalt-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724f9b394d6e70354b39036df90386a823da2e5874f9ecb0fc0b81f130e3571e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125040"
---
# <a name="imstscnonscriptableportablesalt-property"></a>IMsTscNonScriptable::P ortableSalt-Eigenschaft

Diese Eigenschaft wird nicht mehr unterstützt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue portierbare Salt-Teil für ein portierbares codiertes Kennwort.

## <a name="error-codes"></a>Fehlercodes

Gibt **E \_ NOTIMPL zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                              |
| Ende des Supports (Server)<br/>    | Nicht unterstützt<br/>                                                              |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | \_IID-IMsTscNonScriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[**PortablePassword**](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





