---
title: Imstscax cipherstärke (Eigenschaft)
description: Ruft die maximale Verschlüsselungsstärke des aktuellen Steuer Elements ab.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Eigenschaft "cipherstärke" Remotedesktopdienste
- Eigenschaften Remotedesktopdienste cipherstärke, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, cipherstärke (Eigenschaft)
- Cipherstärke-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391599"
---
# <a name="imstscaxcipherstrength-property"></a>Imstscax:: cipherstärke (Eigenschaft)

Ruft die maximale Verschlüsselungsstärke des aktuellen Steuer Elements ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Verschlüsselungsstärke.

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Bei Remotedesktop-Webverbindung ist die Verschlüsselungsstärke immer 128, da das Remotedesktop ActiveX-Steuerelement die Verschlüsselung bis einschließlich 128 Bits unterstützt. Das 128-Bit-Steuerelement kann weiterhin eine Verbindung mit 56 Bit Encryption Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern herstellen.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

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

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





