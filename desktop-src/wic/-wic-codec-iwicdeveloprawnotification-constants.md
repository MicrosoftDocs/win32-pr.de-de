---
description: Flags, die von IWICDevelopRawNotificationCallback verwendet werden, um anzugeben, welche Member geändert wurden.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: IWICDevelopRawNotificationCallback-Konstanten (wincodec. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8bf5d7cb2f4ac0e6fddd1f2e9151c95143b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960498"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>IWICDevelopRawNotificationCallback-Konstanten

Flags, die von [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) verwendet werden, um anzugeben, welche Member geändert wurden.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**Wicrawchangenotifizierung \_ Exposurecompensation**</dt> <dt>0x00000001</dt> </dl>             | Maske, die verwendet wird, um eine Änderung der Gefährdungen von Änderungen<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**Wicrawchangenotifizierung \_ Namedwhitepoint**</dt> <dt>0x00000002</dt> </dl>                                 | Maske, die verwendet wird, um eine [**wicnamedwhitepoint**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint) -Änderung zu melden.<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**Wicrawchangenotifizierung \_ Kelvinwhitepoint**</dt> <dt>0x00000004</dt> </dl>                             | Maske, die zum Melden eines Kelvin-weißen Punkts verwendet wird.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**Wicrawchangenotifizierung \_ Rgbwhitepoint**</dt> <dt>0x00000008</dt> </dl>                                         | Maske, die zum Melden einer RGB-Änderung des weißen Punkts verwendet wird.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**Wicrawchangenotifizierung \_ Kontrast**</dt> <dt>0x00000010</dt> </dl>                                                             | Maske, die zum Melden einer Kontrast Änderung verwendet wird.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**Wicrawchangenotifizierung \_ Gamma**</dt> <dt>0x00000020</dt> </dl>                                                                         | Maske, die zum Melden einer Gamma Änderung verwendet wird.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**Wicrawchangenotifizierung \_ Schärfe**</dt> <dt>0x00000040</dt> </dl>                                                         | Maske, die zum Melden einer Schärfe Änderung verwendet wird.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**Wicrawchangenotifizierung \_ Sättigung**</dt> <dt>0x00000080</dt> </dl>                                                     | Maske, die zum Melden einer Sättigungs Änderung verwendet wird.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**Wicrawchangenotifizierung \_ Tint**</dt> <dt>0x00000100</dt> </dl>                                                                             | Maske, die zum Melden einer Tönungs-Änderung verwendet wird.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**Wicrawchangenotifizierung \_ NoiseReduction**</dt> <dt>0x00000200</dt> </dl>                                     | Maske, die zum Melden einer Rausch Änderungs Änderung verwendet wird.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**Wicrawchangenotifizierung \_ DestinationColorContext**</dt> <dt>0x00000400</dt> </dl> | Maske, die zum Melden einer Ziel Farb Kontext Änderung verwendet wird.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**Wicrawchangenotifizierung \_ Tonecurve**</dt> <dt>0x00000800</dt> </dl>                                                         | Maske, die zum Melden einer Änderung der Tonkurve verwendet wird.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**Wicrawchangenotifizierung \_ Drehung**</dt> <dt>0x00001000</dt> </dl>                                                             | Maske, die zum Melden einer [**wicrawrotationfunktionalitäten**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) -Änderung verwendet wird.<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**Wicrawchangenotifizierung \_ RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Maske, die verwendet wird, um eine [**wicrawrendermode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) -Änderung zu melden.<br/>                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincodec. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




