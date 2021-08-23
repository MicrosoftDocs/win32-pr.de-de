---
description: Flags, die von IWICDevelopRawNotificationCallback verwendet werden, um anzugeben, welche Member geändert wurden.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: IWICDevelopRawNotificationCallback-Konstanten (Wincodec.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a99ea21ccafdb3961387013d0f6d9f466e48ffe542a3349af7e658b1b1786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592460"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>IWICDevelopRawNotificationCallback-Konstanten

Flags, die von [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) verwendet werden, um anzugeben, welche Member geändert wurden.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                            | Beschreibung                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_ ExposureCompensation**</dt> <dt>0x00000001</dt> </dl>             | Maske, die verwendet wird, um eine Änderung der Belichtungskompensierung zu melden.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ NamedWhitePoint**</dt> <dt>0x00000002</dt> </dl>                                 | Maske, die zum Melden einer [**WICNamedWhitePoint-Änderung**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint) verwendet wird.<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ KelvinWhitePoint**</dt> <dt>0x00000004</dt> </dl>                             | Maske, die verwendet wird, um eine Kelvin-Weißpunktänderung zu melden.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ RGBWhitePoint**</dt> <dt>0x00000008</dt> </dl>                                         | Maske, die verwendet wird, um eine RGB-Weißpunktänderung zu melden.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_ Kontrast**</dt> <dt>0x00000010</dt> </dl>                                                             | Maske, die verwendet wird, um eine Kontraständerung zu melden.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_ Gamma**</dt> <dt>0x00000020</dt> </dl>                                                                         | Maske, die verwendet wird, um eine Gammaänderung zu melden.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_ Schärfe**</dt> <dt>0x00000040</dt> </dl>                                                         | Maske, die verwendet wird, um eine Schärfeänderung zu melden.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>Sättigungs-0x00000080</dt> </dl>                                                     | Maske, die verwendet wird, um eine Sättigungsänderung zu melden.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_ Farbton**</dt> <dt>0x00000100</dt> </dl>                                                                             | Maske, die verwendet wird, um eine Farbtonänderung zu melden.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_ NoiseReduction-0x00000200**</dt> <dt></dt> </dl>                                     | Maske, die verwendet wird, um eine Änderung der Rauschunterdrückung zu melden.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_ DestinationColorContext**</dt> <dt>0x00000400</dt> </dl> | Maske, die verwendet wird, um eine Änderung des Zielfarbkontexts zu melden.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_ ToneCurve**</dt> <dt>0x00000800</dt> </dl>                                                         | Maske, die verwendet wird, um eine Änderung der Tonkurve zu melden.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_ Rotation**</dt> <dt>0x00001000</dt> </dl>                                                             | Maske, die zum Melden einer [**WICRawRotationCapabilities-Änderung**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) verwendet wird.<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_ RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Maske, die zum Melden einer [**WICRawRenderMode-Änderung**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) verwendet wird.<br/>                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincodec.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




