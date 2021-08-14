---
title: IMsRdpClientAdvancedSettings BitmapVirtualCacheSize-Eigenschaft
description: Gibt die Größe der persistenten Bitmapcachedatei in Megabyte an, die für die Farbe 8 Bits pro Pixel verwendet werden soll.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
- BitmapVirtualCacheSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , BitmapVirtualCacheSize-Eigenschaft
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
ms.openlocfilehash: 45ec0d02e71849af88212db733ee205cb26f8c72a5c67c00acaef528bf086423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353174"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a>IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize-Eigenschaft

Gibt die Größe der persistenten Bitmapcachedatei in Megabyte an, die für die Farbe 8 Bits pro Pixel verwendet werden soll.

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

Die neue Cachegröße. Die gültigen Werte sind 1 bis einschließlich 32. Beachten Sie, dass die maximale Größe für alle virtuellen Cachedateien 128 MB beträgt.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

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

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





