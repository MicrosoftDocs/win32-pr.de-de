---
title: IMsTscNonScriptable BinarySalt-Eigenschaft
description: Diese Eigenschaft ist nicht mehr für die Verwendung verfügbar. | IMsTscNonScriptable BinarySalt-Eigenschaft
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- BinarySalt-Eigenschaft Remotedesktopdienste
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsTscNonScriptable-Schnittstelle
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , MsTscAx-Objekt
- MsTscAx-Objekt Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
- BinarySalt-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , BinarySalt-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e58618a59beb484e09967af42bd75c527a87693d7aed25cb86857e776c382d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756917"
---
# <a name="imstscnonscriptablebinarysalt-property"></a>IMsTscNonScriptable::BinarySalt-Eigenschaft

Diese Eigenschaft ist nicht mehr für die Verwendung verfügbar.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue binäre Salt-Teil für ein binär codiertes Kennwort.

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



## <a name="see-also"></a>Weitere Informationen

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
</dt> </dl>

 

 





