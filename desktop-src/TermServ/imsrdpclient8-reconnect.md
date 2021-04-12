---
title: IMsRdpClient8 Reconnect-Methode
description: Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Reconnect-Methode Remotedesktopdienste
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519247"
---
# <a name="imsrdpclient8reconnect-method"></a>IMsRdpClient8:: Reconnect-Methode

Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her. Das-Steuerelement muss bereits mit einer Remote Sitzung verbunden sein, damit diese Methode erfolgreich ausgeführt werden konnte.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulwidth* \[ in\]
</dt> <dd>

Typ: **ulong**

Die neue Breite des Desktops in Pixel. Informationen zu Wert Einschränkungen finden Sie in der [**desktopwidth**](imstscax-desktopwidth.md) -Eigenschaft.

</dd> <dt>

*ulheight* \[ in\]
</dt> <dd>

Typ: **ulong**

Die neue Höhe des Desktops in Pixel. Informationen zu Wert Einschränkungen finden Sie in der [**desktopheight**](imstscax-desktopheight.md) -Eigenschaft.

</dd> <dt>

*preconnectstatus* \[ Out, retval\]
</dt> <dd>

Typ: **[**controlreconnectstatus**](controlreconnectstatus.md) \** _

Ein Zeiger auf eine [_ *controlreconnectstatus* *](controlreconnectstatus.md) -Variable, die den Status des Vorgangs zum erneuten Verbinden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 ist als 4247e044-9271-43a9-bc49-e2ad9e855d62 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**Controlreconnectstatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





