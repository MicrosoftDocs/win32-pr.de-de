---
title: IMsTscAx DesktopWidth (Eigenschaft)
description: Gibt die Breite des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel an.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- DesktopWidth-Remotedesktopdienste
- DesktopWidth-Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, DesktopWidth-Eigenschaft
- DesktopWidth-Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, DesktopWidth-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca982303208bb2badecf210c9590f627a7b3b57c5acd9ecd7f8fee0bbb70ec93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058843"
---
# <a name="imstscaxdesktopwidth-property"></a>IMsTscAx::D esktopWidth-Eigenschaft

Gibt die Breite des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Breite in Pixel.

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Das Festlegen **der DesktopWidth-Eigenschaft** ist optional, muss jedoch festgelegt werden, bevor die Verbinden [**wird.**](imstscax-connect.md) Wenn keine Desktopbreite angegeben oder auf 0 (null) festgelegt ist, wird die Desktopbreite auf die Breite des Steuerelements festgelegt. Die Mindest- und Höchstwerte hängen von der Betriebssystemversion des Remotedesktop ab.

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

Nachdem eine Verbindung hergestellt wurde, ändern änderungen an der Breite des Steuerelements nicht die Breite des Remotedesktops. Stattdessen werden vom Steuerelement bildlaufleisten angezeigt oder der Remotedesktop entsprechend centert. Verwenden Sie die [**IMsRdpClient8::Reconnect-Methode,**](imsrdpclient8-reconnect.md) um die Desktopgröße einer aktiven Verbindung zu ändern.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

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

 

 





