---
title: IMsRdpClientAdvancedSettings7 VideoPlaybackMode-Eigenschaft
description: Gibt einen Wert an, der den Videowiedergabemodus angibt, oder ruft diesen ab.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- VideoPlaybackMode-Eigenschaft Remotedesktopdienste
- VideoPlaybackMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , VideoPlaybackMode-Eigenschaft
- VideoPlaybackMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , VideoPlaybackMode-Eigenschaft
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
ms.openlocfilehash: 353cf72822ac91686cb5a08edf5ca6a5e25b24ff8e544ff79bdd8a2085f761fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607817"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>IMsRdpClientAdvancedSettings7::VideoPlaybackMode-Eigenschaft

Gibt einen Wert an, der den Videowiedergabemodus angibt, oder ruft diesen ab.

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

Ein -Wert, der den Videowiedergabemodus angibt.

Mögliche Werte sind:

<dt>

1
</dt> <dd>

Der Standardwiedergabemodus für Videos. Wenn der Videowiedergabemodus auf diesen Wert festgelegt ist, wird die Videoumleitung durch die [**AudioRedirectionMode-Eigenschaft**](imsrdpclientsecuredsettings-autoredirectionmode.md) gesteuert. Wenn die **AudioRedirectionMode-Eigenschaft** auf **AUDIO MODE \_ \_ REDIRECT** festgelegt ist, wird das Video decodiert und auf dem Client gerendert.

</dd> <dt>

0
</dt> <dd>

Die Videowiedergabeumleitung ist deaktiviert, auch wenn [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) auf **AUDIO MODE \_ \_ REDIRECT** festgelegt ist. In diesem Modus wird das Video decodiert und auf dem RD-Sitzungshost-Server gerendert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





