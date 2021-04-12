---
description: Implementieren von IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementieren von IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218571"
---
# <a name="implementing-iwicdevelopraw"></a>Implementieren von IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

Die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle stellt Verarbeitungsoptionen für die Rohbild Verarbeitung bereit. Alle Rohdaten-CODECs müssen die **IWICDevelopRaw** -Schnittstelle unterstützen. Einige unformatierte Codecs können möglicherweise nicht jede Einstellung unterstützen, die von dieser Schnittstelle verfügbar gemacht wird, aber Sie sollten alle Einstellungen unterstützen, die Ihr Codec ausführen kann. Jeder unformatierte Codec muss [**mindestens die Methoden**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) "-Methode" und " [**ltrendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) " implementieren.

Außerdem werden für unformatierte Codecs dringend einige Methoden und Schnittstellen empfohlen, die für andere Codecs optional sind. Hierzu gehören die Methoden [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) und [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) in der Decoder-Klasse auf Container-Ebene und die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -Schnittstelle in der Klasse "decodieren" auf Frame-Ebene.

Die Einstellungen, die mithilfe der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Methoden festgelegt werden, sollten vom Codec auf eine Weise persistent gespeichert werden, die mit der beibehaltenen Verwendung anderer Metadaten konsistent ist, aber Sie sollten niemals die ursprünglichen "als shot"-Einstellungen überschreiben. Wenn Sie die Metadaten beibehalten und [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) und [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)implementieren, können Sie rohdatenverarbeitungs Anwendungen zum Abrufen und Anwenden von Verarbeitungseinstellungen Sitzungs übergreifend aktivieren.

Der Hauptzweck der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle besteht darin, Anwendungsentwicklern das Erstellen einer Benutzeroberfläche zum Anpassen von unformatierten Parametern zu ermöglichen, die so konsistent wie möglich über verschiedene Codecs hinweg funktionieren. Angenommen, ein Endbenutzer passt die Parameter mit einem Schieberegler-Steuerelement an, wobei die minimalen und maximalen Werte dem minimalen und maximalen Bereich für den Parameter zugeordnet werden. Um dies zu unterstützen, sollten Sie alle Parameterbereiche als linear behandeln. Um sicherzustellen, dass die Schieberegler-Steuerelemente nicht übermäßig sensibel sind, sollten Sie auch so weit wie möglich einen Bereich für jeden Parameter unterstützen und dabei mindestens 50 Prozent des maximal möglichen Bereichs abdecken. Beispiel: Wenn der maximal mögliche Kontrastbereich von "rein grau" zu "schwarz" und "weiß" ist, wobei der Standardwert "0,0" zugeordnet wird, würde der von einem Codec unterstützte Mindestbereich von mindestens Mitte zwischen dem Standardwert und dem reinen grauen am unteren Ende (– 1,0) liegen 1,0.


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



-   [Queryrawcapabilitiesinfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/getcurrentparameterrgb, Set/GetNamedWhitePoint, Set/GetWhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/getschärding](#setgetsharpness)
-   [Set/getationations](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>Queryrawcapabilitiesinfo

[**Queryrawcapabilitiesinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) gibt den Satz unterstützter Funktionen für diese Rohdatendatei zurück. Die [**wicrawcapabilitiesinfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) -Struktur ist wie folgt definiert:


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



Die in dieser Struktur verwendete [**wicrawfunktionalitäten**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) -Enumeration wird wie folgt definiert:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Das letzte Feld ist eine [**wicrawrotationfunktionalitäten**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) -Enumeration, die wie folgt definiert ist:


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

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) ermöglicht dem Benutzer, anzugeben, ob als Erstellungseinstellungen verwendet werden sollen, Benutzer angepasste Einstellungen verwendet oder der Decoder aufgefordert werden soll, das Bild automatisch zu korrigieren.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) gibt ein **IPropertyBag2** mit dem aktuellen Parametersatz zurück. Der Aufrufer kann dann diesen Parametersatz an den Encoder übergeben, der als Codierungsoptionen verwendet werden soll.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) und [**eintexposurecompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) geben die auf die endgültige Ausgabe anzuwendende ausgabenkompensierung an. Der gültige Bereich für EV ist – 5,0 bis + 5,0 Stopps.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/getcurrentparameterrgb, Set/GetNamedWhitePoint, Set/GetWhitePointKelvin

Diese Funktionen bieten alle Möglichkeiten zum Aufrufen und Festlegen des weißen Punkts, entweder als RGB-Wert, als vordefinierter benannter Wert oder als Kelvin-Wert. Der zulässige Bereich für Kelvin ist 1.500 – 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) und [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) geben den Kontrast an, der auf die Ausgabe angewendet werden soll. Der gültige Bereich für die Angabe des Kontrasts ist – 1,0 bis + 1,0, wobei der Standard Kontrast 0,0 ist.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) und [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) geben das anzuwendende Gamma an. Der gültige Bereich für Gamma ist 0,2 bis 5,0, wobei 1,0 der Standardwert ist. Gamma wird in der Regel mit der herkömmlichen Gamma Power-Funktion implementiert (eine lineare Energie Funktion mit Unity-Gewinn). Die Helligkeit wird mit zunehmender Gamma Steigerung erhöht und verringert, wenn Gamma den Wert 0 erreicht. (Beachten Sie, dass der minimale Wert ungleich 0 (null) ist, weil NULL in herkömmlichen Gamma Berechnungen zu einem Fehler aufgrund einer Division durch Null führt. Das logische Mindestlimit beträgt 1/Max, weshalb das Minimalwert 0,2 ist.)

### <a name="setgetsharpness"></a>Set/getschärding

[**Getschärding**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) und [**setschärding**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) geben den Umfang der anzuwendenden Schärfe an. Der gültige Bereich ist – 1,0 bis + 1,0, wobei 0,0 der Standardwert für die Schärfe ist, und – 1,0, was überhaupt keine Schärfe angibt.

### <a name="setgetsaturation"></a>Set/getationations

" [**Getationations**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) " und "die fest [**legung**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) " geben den Umfang der anzuwendenden Sättigung an. Der gültige Bereich zum Angeben der Sättigung ist – 1,0 bis + 1,0, wobei 0,0 eine normale Sättigung ist, – 1,0 die vollständige Überlastung darstellt, und + 1,0, die eine vollständige Sättigung darstellt.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) und [**settint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) geben das anzuwendende Tönungs an, wenn ein grünes/Magenta-Bias angezeigt wird. Der gültige Bereich liegt zwischen – 1,0 und + 1,0, wobei grün auf der negativen Seite der Skala und Magenta auf der positiven Seite liegt. Die Tönungs-Skala ist als orthogonal bis Color-Temperatur definiert.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) und [**setnoisereduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) geben die Menge der anzuwendenden Rauschunterdrückung an. Der gültige Bereich für ist – 1,0 bis + 1,0.0,0 gibt die Standardmenge der Rauschunterdrückung an, – 1,0 bedeutet, dass keine Rauschunterdrückung erfolgt und + 1,0 eine maximale Rauschunterdrückung angibt.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) gibt das Farbprofil an, das auf das Bild angewendet werden soll. Sie können [**getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) aufrufen, um das aktuelle Farbprofil abzurufen.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) und [**settonecurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) geben Sie die anzuwendende Tonkurve an. Angenommen, lineare Interpolationen zwischen Punkten. **PToneCurve** ist eine [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) -Struktur, die ein Array aus [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) -Strukturen und eine Anzahl der Punkte im Array enthält.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Ein [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) enthält einen Eingabe Wert und einen Ausgabewert.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Wenn der Aufrufer **null** im *pToneCurve* -Parameter übergibt, sollten Sie die erforderliche Größe für die [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) im *pcbActualToneCurveBufferSize* -Parameter zurückgeben.

### <a name="setgetrotation"></a>Set/GetRotation

" [**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) " und " [**ttrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) " geben den Grad der anzuwendenden Drehung an. Eine Drehung von 90,0 würde eine Drehung von 90 Grad im Uhrzeigersinn angeben. (Der Unterschied zwischen der Verwendung von "  **SetRotation** " und dem Festlegen der Drehung mithilfe der [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) -Methode besteht darin, dass der Drehungs Winkel, der mithilfe von " **SetRotation** " festgelegt wird, vom Codec beibehalten werden soll

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) und [**setrendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) geben die Qualität der Ausgabe an, die der Aufrufer benötigt. Wenn ein Benutzerparameter anpasst, sollte die Anwendung eine sehr schnelle Näherung des tatsächlichen Bilds anzeigen, wenn die Änderungen angewendet werden. Zu diesem Zweck wird das Bild normalerweise bei der Bildschirmauflösung oder weniger angezeigt, anstatt bei der tatsächlichen Bildauflösung, um dem Benutzer sofortiges Feedback zu geben. Dies ist der Fall, wenn eine Anwendung die Qualität des Entwurfs Modus anfordern würde, sodass dies sehr schnell sein sollte. Wenn der Benutzer alle Änderungen vorgenommen hat, Sie in der Vorschau im Entwurfs Modus angezeigt haben und sich entschieden haben, das vollständige Image mit den aktuellen Einstellungen zu decodieren, fordert die Anwendung einen Decodieren der optimalen Qualität an. Dies wird in der Regel auch zum Drucken angefordert. Wenn ein angemessener Kompromiss zwischen Geschwindigkeit und Qualität erforderlich ist, fordert die Anwendung die normale Qualität an.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registriert eine Rückruffunktion, die der Decoder aufruft, wenn sich einer der rohverarbeitungs Parameter ändert. Die Signatur für [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) verfügt nur über eine Methode, die als " [**Benachrichtigen**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify)" bezeichnet wird. **Notify** weist einen einzelnen Parameter auf, bei dem es sich um eine Maske handelt, die angibt, welche der rohverarbeitungs Parameter geändert wurden.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Ein-oder-Vorgang wird für die folgenden Werte für die notificationmask ausgeführt.


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

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementieren eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



