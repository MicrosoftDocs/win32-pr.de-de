---
title: Imsrdpclientadvancedsettings BitmapVirtualCache16BppSize (Eigenschaft)
description: Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für die 15-und 16-Bit-pro-Pixel-High-Color-Einstellungen verwendet werden soll.
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache16BppSize-Eigenschaft Remotedesktopdienste
- BitmapVirtualCache16BppSize-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338709"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a>Imsrdpclientadvancedsettings:: BitmapVirtualCache16BppSize-Eigenschaft

Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für die 15-und 16-Bit-pro-Pixel-High-Color-Einstellungen verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Cache Größe. Gültige Werte sind 1 bis 32 einschließlich, der Standardwert ist 20. Beachten Sie, dass die maximale Größe für alle virtuellen Cache Dateien 128 MB beträgt.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Zu den zugehörigen Eigenschaften gehören die **bitmapvirtualcachesize** -Eigenschaft und die **BitmapVirtualCache24BppSize** -Eigenschaft.

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

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





