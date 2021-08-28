---
title: IMsTscAx DesktopHeight (Eigenschaft)
description: Gibt die Höhe des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel an.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- DesktopHeight-Remotedesktopdienste
- DesktopHeight-Eigenschaft Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
- DesktopHeight-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, DesktopHeight-Eigenschaft
- DesktopHeight-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , DesktopHeight-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e55d5a1f529435f0cdf6db3dcf801e7f24dda1a69e0bc1cad393942b672d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513100"
---
# <a name="imstscaxdesktopheight-property"></a>IMsTscAx::D esktopHeight-Eigenschaft

Gibt die Höhe des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Höhe in Pixel.

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Das Festlegen **der DesktopHeight-Eigenschaft** ist optional, muss jedoch vor dem Aufrufen der Verbinden [**festgelegt**](imstscax-connect.md) werden. Wenn keine Desktophöhe angegeben oder auf 0 (null) festgelegt ist, wird die Desktophöhe auf die Höhe des Steuerelements festgelegt. Die Mindest- und Höchstwerte hängen von der Betriebssystemversion des Remotedesktop ab.

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

Mindestens 200, maximal 8192

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

Mindestens 200, maximal 2048

</dd> <dt>

Windows Vista
</dt> <dd>

Mindestens 200, maximal 1200

</dd> </dl>

Nachdem eine Verbindung hergestellt wurde, ändern alle Änderungen an der Höhe des Steuerelements die Höhe des Remotedesktops nicht. Stattdessen werden vom Steuerelement bildlaufleisten angezeigt oder der Remotedesktop entsprechend centert. Verwenden Sie die [**IMsRdpClient8::Reconnect-Methode,**](imsrdpclient8-reconnect.md) um die Desktopgröße einer aktiven Verbindung zu ändern.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx ist als 8C11EFAE-92C3-11D1-BC1E-00C04FA31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





