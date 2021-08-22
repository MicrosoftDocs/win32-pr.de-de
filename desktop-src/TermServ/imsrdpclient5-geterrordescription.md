---
title: IMsRdpClient5 GetErrorDescription-Methode
description: Ruft die Fehlerbeschreibung für die Sitzungstrennungsereignisse ab.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- GetErrorDescription-Methode Remotedesktopdienste
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , GetErrorDescription-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197025b4cfb842cf4ca38af64124c02415240ac6fc878f9c121d4e228b77f5b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001488"
---
# <a name="imsrdpclient5geterrordescription-method"></a>IMsRdpClient5::GetErrorDescription-Methode

Ruft die Fehlerbeschreibung für die Sitzungstrennungsereignisse ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*disconnectReason* \[ In\]
</dt> <dd>

Der Grund für die Trennung.

</dd> <dt>

*extendedDisconnectReason* \[ In\]
</dt> <dd>

Enthält ausführliche Informationen dazu, warum eine Trennung initiiert wurde.

</dd> <dt>

*pBstrErrorMsg* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BSTR-Variable,** die den Fehlermeldungstext empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-b922-e06a28ecd8bf definiert.<br/>       |



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

 

 





