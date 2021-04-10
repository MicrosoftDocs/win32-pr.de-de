---
title: Imsrdpclientadvancedsettings bitmapvirtualcachesize (Eigenschaft)
description: Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für 8-Bit-pro-Pixel-Farbe verwendet werden soll.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, bitmapvirtualcachesize-Eigenschaft
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
- Bitmapvirtualcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, bitmapvirtualcachesize (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040332"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a>Imsrdpclientadvancedsettings:: bitmapvirtualcachesize-Eigenschaft

Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für 8-Bit-pro-Pixel-Farbe verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Cache Größe. Gültige Werte sind 1 bis 32 einschließlich. Beachten Sie, dass die maximale Größe für alle virtuellen Cache Dateien 128 MB beträgt.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**BitmapVirtualCache16BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[**BitmapVirtualCache24BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





