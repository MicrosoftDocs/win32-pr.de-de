---
description: Implementieren von IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementieren von IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a78705fcfb53651d1099d01d17d9ddff554df9632a5cc322db229bc04d38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965009"
---
# <a name="implementing-iwicdevelopraw"></a>Implementieren von IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

Die [**IWICDevelopRaw-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) macht Verarbeitungsoptionen verfügbar, die spezifisch für die rohe Bildverarbeitung sind. Alle unformatierten Codecs müssen die **IWICDevelopRaw-Schnittstelle** unterstützen. Einige unformatierte Codecs können möglicherweise nicht jede Einstellung unterstützen, die von dieser Schnittstelle verfügbar gemacht wird. Sie sollten jedoch alle Einstellungen unterstützen, die Ihr Codec ausführen kann. Jeder unformatierte Codec muss mindestens die [**Methoden SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) und [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) implementieren.

Darüber hinaus werden einige Methoden und Schnittstellen, die für andere Codecs optional sind, für unformatierte Codecs dringend empfohlen. Dazu gehören die [**Methoden GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) und [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) für die Decoderklasse auf Containerebene und die [**IWICBitmapSourceTransform-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) für die Decodierungsklasse auf Frameebene.

Einstellungen, die mithilfe der [**IWICDevelopRaw-Methoden**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) festgelegt werden, sollten vom Codec auf eine Weise beibehalten werden, die mit der Art und Weise konsistent ist, wie andere Metadaten beibehalten werden, aber Sie sollten die ursprünglichen "As Shot"-Einstellungen nie überschreiben. Indem Sie die Metadaten beibehalten und [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) und [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)implementieren, ermöglichen Sie Unformatierungsverarbeitungsanwendungen, Verarbeitungseinstellungen sitzungsübergreifend abzurufen und anzuwenden.

Ein Hauptzweck der [**IWICDevelopRaw-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) besteht darin, Anwendungsentwicklern das Erstellen einer Benutzeroberfläche zum Anpassen von rohen Parametern zu ermöglichen, die für verschiedene Codecs so konsistent wie möglich funktionieren. Angenommen, ein Endbenutzer passt die Parameter mithilfe eines Schieberegler-Steuerelements an, wobei die minimalen und maximalen Werte den minimalen und maximalen Bereichen für den Parameter zugeordnet sind. Um dies zu unterstützen, sollten Sie alle Parameterbereiche als linear behandeln. Um sicherzustellen, dass die Schieberegler-Steuerelemente nicht übermäßig empfindlich sind, sollten Sie auch einen möglichst breiten Bereich für jeden Parameter unterstützen, der mindestens 50 Prozent des maximal möglichen Bereichs abdeckt. Wenn der maximal mögliche Kontrastbereich beispielsweise von rein grau bis rein schwarz und weiß liegt und der Standardwert 0,0 zugeordnet wird, würde der von einem Codec unterstützte Mindestbereich von mindestens der Hälfte zwischen dem Standardwert und rein grau am unteren Ende (–1,0) bis mindestens zur Hälfte zwischen dem Standardwert und reinem Schwarz und Weiß am hohen Ende (+1,0) liegen.


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) gibt die unterstützten Funktionen für diese Rohdatendatei zurück. Die [**WICRawCapabilitiesInfo-Struktur**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) ist wie folgt definiert:


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



Die in dieser Struktur verwendete [**WICRawCapabilities-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) ist wie folgt definiert:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Das letzte Feld ist eine [**WICRawRotationCapabilities-Enumeration,**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) die wie folgt definiert ist:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) ermöglicht es dem Benutzer anzugeben, ob As Shot-Einstellungen verwendet, vom Benutzer angepasste Einstellungen verwendet werden sollen, oder den Decoder anzufordern, das Bild automatisch zu korrigieren.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) gibt ein **IPropertyBag2** mit dem aktuellen Parametersatz zurück. Der Aufrufer kann diesen Parameter dann an den Encoder übergeben, der als Encoderoptionen verwendet werden soll.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) und [**SetExposureCompensation geben die Gefährdungskompensierung**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) an, die auf die endgültige Ausgabe angewendet werden soll. Der gültige Bereich für EV beträgt –5,0 bis +5,0 Stopps.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Diese Funktionen bieten alle Möglichkeiten zum Abrufen und Festlegen des Weißen Punkts, entweder als RGB-Wert, als voreingestellter benannter Wert oder als Kelvin-Wert. Der zulässige Bereich für Kelvin liegt zwischen 1.500 und 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) und [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) geben den Kontrast an, der auf die Ausgabe angewendet werden soll. Der gültige Bereich zum Angeben des Kontrasts ist –1,0 bis +1,0, wobei der Standardkontrast 0,0 ist.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) und [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) geben das zu übernehmende Gamma an. Der gültige Bereich für Gamma beträgt 0,2 bis 5,0, wobei 1,0 der Standardwert ist. Gamma wird in der Regel mithilfe der herkömmlichen Gamma-Potenzfunktion implementiert (eine lineare Potenzfunktion mit Unity-Gewinn). Die Helligkeit wird mit steigendem Gamma erhöht und verringert, wenn sich Gamma 0 nähert. (Beachten Sie, dass der Mindestwert ungleich 0 (null) ist, da 0 in herkömmlichen Gammaberechnungen zu einem Fehler aufgrund einer Division durch 0 führen würde. Der logische Mindestgrenzwert ist 1/max, weshalb der Mindestwert 0,2 beträgt.)

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) und [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) geben den Umfang der zu übernehmenden Schärfe an. Der gültige Bereich liegt zwischen –1,0 und +1,0, wobei 0,0 die Standardmenge der Schärfung ist und –1,0 keine Schärfe angibt.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) und [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) geben an, wie viel Sättigung angewendet werden soll. Der gültige Bereich zum Angeben der Sättigung ist –1,0 bis +1,0, wobei 0,0 eine normale Sättigung ist, –1,0 die vollständige Desaturierung und +1,0 die vollständige Sättigung darstellt.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) und [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) geben die Tönung an, die auf eine Grün-Magenta-Verzerrung angewendet werden soll. Der gültige Bereich ist –1,0 bis +1,0, wobei Grün auf der negativen Seite der Skala und Magenta auf dem positiven liegt. Die Farbtonskala ist als orthogonale farbliche Temperatur definiert.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) und [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) geben an, wie viel Rauschunterdrückung angewendet werden soll. Der gültige Bereich von ist –1,0 bis +1,0, wobei 0,0 die Standardmenge der Rauschunterdrückung, –1,0 keine Rauschunterdrückung und +1,0 die maximale Rauschunterdrückung angibt.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) gibt das Farbprofil an, das auf das Bild angewendet werden soll. Sie können [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) aufrufen, um das aktuelle Farbprofil abzurufen.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) und [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) geben die zu übernehmende Tonkurve an. Angenommen, es wird eine lineare Interpolation zwischen Punkten angenommen. **pToneCurve** ist eine [**WICRawToneCurve-Struktur,**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) die ein Array von [**WICRawToneCurvePoint-Strukturen**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) und eine Anzahl der Punkte im Array enthält.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Ein [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) enthält einen Eingabewert und einen Ausgabewert.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Wenn der Aufrufer **NULL** im *pToneCurve-Parameter* übergibt, sollten Sie die erforderliche Größe für [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) im *parameteractualToneCurveBufferSize-Parameter* zurückgeben.

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) und [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) geben den Grad der Rotation an, der angewendet werden soll. Eine Drehung von 90,0 würde eine Drehung von 90 Grad im Uhrzeigersinn angeben. (Der Unterschied zwischen der Verwendung von **SetRotation** und der Einstellungsrotation mithilfe der [**CopyPixels-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) besteht darin, dass der mit **SetRotation** festgelegte Drehwinkel vom Codec beibehalten werden soll, während das Festlegen der Drehung durch **CopyPixels** nur das Bild im Arbeitsspeicher dreht.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) und [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) geben die Qualitätsstufe der Ausgabe an, die der Aufrufer benötigt. Wenn ein Benutzer Parameter anpasst, sollte die Anwendung eine sehr schnelle Näherung des tatsächlichen Bilds anzeigen, wenn die Änderungen angewendet werden. Zu diesem Zweck wird das Bild in der Regel mit Bildschirmauflösung oder weniger als der tatsächlichen Bildauflösung angezeigt, um dem Benutzer sofortiges Feedback zu geben. Da eine Anwendung die Entwurfsmodusqualität anfordern würde, sollte dies sehr schnell erfolgen. Wenn der Benutzer alle Änderungen vorgenommen hat, sie im Entwurfsmodus in der Vorschau angezeigt und sich entschieden hat, das vollständige Image mit den aktuellen Einstellungen zu decodieren, fordert die Anwendung eine Best Quality-Decodierung an. Dies wird in der Regel auch für den Druck angefordert. Wenn ein angemessener Kompromiss zwischen der Geschwindigkeit einer Qualität erforderlich ist, fordert die Anwendung normale Qualität an.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registriert eine Rückruffunktion für den Decoder, die aufgerufen werden soll, wenn sich einer der Raw-Verarbeitungsparameter ändert. Die Signatur für [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) verfügt nur über eine Methode namens [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** verfügt über einen einzelnen Parameter, bei dem es sich um eine Maske handelt, die angibt, welche der Rohdatenverarbeitungsparameter geändert wurden.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Ein OR-Vorgang wird für die folgenden Werte für notificationMask ausgeführt.


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementieren eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



