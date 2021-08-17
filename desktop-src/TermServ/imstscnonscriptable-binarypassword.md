---
title: IMsTscNonScriptable BinaryPassword (Eigenschaft)
description: Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar. | IMsTscNonScriptable BinaryPassword (Eigenschaft)
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- BinaryPassword-Remotedesktopdienste
- BinaryPassword-Eigenschaft Remotedesktopdienste , IMsTscNonScriptable-Schnittstelle
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Eigenschaft Remotedesktopdienste , MsTscAx-Objekt
- MsTscAx-Objekt Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
- BinaryPassword-Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , BinaryPassword-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aef3cb62a6ab2c72d39a79ee4cd6e5d64192ae24bc8ef201da603cdbc528859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757126"
---
# <a name="imstscnonscriptablebinarypassword-property"></a>IMsTscNonScriptable::BinaryPassword (Eigenschaft)

Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Kennwortteil im binär codierten Format.

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
| IID<br/>                      | IID \_ IMsTscNonScriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.<br/> |



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

 

 





