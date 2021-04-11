---
title: Imsrdpclient colortiefe-Eigenschaft
description: Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Colortiefe-Eigenschaft Remotedesktopdienste
- Colortiefe-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105878"
---
# <a name="imsrdpclientcolordepth-property"></a>Imsrdpclient:: colortiefe-Eigenschaft

Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Farbtiefe. Die Werte umfassen 8, 15, 16, 24 und 32 Bits pro Pixel.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methoden erfolgreich sind, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





