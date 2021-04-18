---
title: IMsRdpClientAdvancedSettings7 videoplaybackmode (Eigenschaft)
description: Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Videoplaybackmode-Eigenschaft Remotedesktopdienste
- Videoplaybackmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, videoplaybackmode (Eigenschaft)
- Videoplaybackmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, videoplaybackmode (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392226"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>IMsRdpClientAdvancedSettings7:: videoplaybackmode (Eigenschaft)

Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der den Videowiedergabe Modus angibt.

Mögliche Werte sind:

<dt>

1
</dt> <dd>

Der Standardmodus für die Videowiedergabe. Wenn der Videowiedergabe Modus auf diesen Wert festgelegt ist, wird die Video Umleitung von der [**audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md) -Eigenschaft gesteuert. Wenn die **audioredirectionmode** -Eigenschaft auf **audiomodusumleitung \_ \_** festgelegt ist, wird das Video decodiert und auf dem Client gerendert.

</dd> <dt>

0
</dt> <dd>

Die Umleitung der Video Wiedergabe ist deaktiviert, auch wenn [**audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md) auf **audiomodusumleitung \_ \_** festgelegt ist. In diesem Modus wird das Video auf dem RD-Sitzungshost Server decodiert und gerendert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





