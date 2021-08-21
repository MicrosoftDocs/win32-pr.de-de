---
title: IMsRdpClientAdvancedSettings BitmapVirtualCache24BppSize (Eigenschaft)
description: Gibt die Größe der persistenten Bitmapcachedatei in Megabyte an, die für die Einstellung mit hoher Farbe von 24 Bit pro Pixel verwendet werden soll.
ms.assetid: 5891c90d-f463-4f27-b212-351ebf21ae00
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache24BppSize-Remotedesktopdienste
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
- BitmapVirtualCache24BppSize-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , BitmapVirtualCache24BppSize (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache24BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e984eef21fa74aa3f3134f19c1d6e7503a24ec9fb67e0ef3bfb0daa6330cfcd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353271"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache24bppsize-property"></a>IMsRdpClientAdvancedSettings::BitmapVirtualCache24BppSize (Eigenschaft)

Gibt die Größe der persistenten Bitmapcachedatei in Megabyte an, die für die Einstellung mit hoher Farbe von 24 Bit pro Pixel verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BitmapVirtualCache24BppSize(
  [in]  LONG bitmapVirtualCache24BppSize
);

HRESULT get_BitmapVirtualCache24BppSize(
  [out] LONG *pbitmapVirtualCache24BppSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Cachegröße. Die gültigen Werte sind 1 bis einschließlich 32, und der Standardwert ist 30. Beachten Sie, dass die maximale Größe für alle virtuellen Cachedateien 128 MB beträgt.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Verwandte Eigenschaften sind die **Eigenschaften BitmapVirtualCacheSize** und **BitmapVirtualCache16BppSize.**

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



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

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





