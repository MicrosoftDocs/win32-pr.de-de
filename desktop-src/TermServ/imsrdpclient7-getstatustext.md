---
title: IMsRdpClient7 GetStatusText-Methode (Openservice.h)
description: Ruft den Statustext für den angegebenen Statuscode ab.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- GetStatusText-Methode Remotedesktopdienste
- GetStatusText-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , GetStatusText-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285190"
---
# <a name="imsrdpclient7getstatustext-method"></a>IMsRdpClient7::GetStatusText-Methode

Ruft den Statustext für den angegebenen Statuscode ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*statusCode* \[ In\]
</dt> <dd>

Ein **UINT,** der den Statuscode angibt, für den der Text abgerufen werden soll.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Die Adresse eines **BSTR,** der den Statustext empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Openservice.h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.<br/>         |



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

 

 





