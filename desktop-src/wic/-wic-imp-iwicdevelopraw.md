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
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="eb065-103">Implementieren von IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="eb065-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="eb065-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="eb065-104">IWICDevelopRaw</span></span>

<span data-ttu-id="eb065-105">Die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle stellt Verarbeitungsoptionen für die Rohbild Verarbeitung bereit.</span><span class="sxs-lookup"><span data-stu-id="eb065-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="eb065-106">Alle Rohdaten-CODECs müssen die **IWICDevelopRaw** -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eb065-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="eb065-107">Einige unformatierte Codecs können möglicherweise nicht jede Einstellung unterstützen, die von dieser Schnittstelle verfügbar gemacht wird, aber Sie sollten alle Einstellungen unterstützen, die Ihr Codec ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="eb065-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="eb065-108">Jeder unformatierte Codec muss [**mindestens die Methoden**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) "-Methode" und " [**ltrendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) " implementieren.</span><span class="sxs-lookup"><span data-stu-id="eb065-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="eb065-109">Außerdem werden für unformatierte Codecs dringend einige Methoden und Schnittstellen empfohlen, die für andere Codecs optional sind.</span><span class="sxs-lookup"><span data-stu-id="eb065-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="eb065-110">Hierzu gehören die Methoden [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) und [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) in der Decoder-Klasse auf Container-Ebene und die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -Schnittstelle in der Klasse "decodieren" auf Frame-Ebene.</span><span class="sxs-lookup"><span data-stu-id="eb065-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="eb065-111">Die Einstellungen, die mithilfe der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Methoden festgelegt werden, sollten vom Codec auf eine Weise persistent gespeichert werden, die mit der beibehaltenen Verwendung anderer Metadaten konsistent ist, aber Sie sollten niemals die ursprünglichen "als shot"-Einstellungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="eb065-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="eb065-112">Wenn Sie die Metadaten beibehalten und [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) und [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)implementieren, können Sie rohdatenverarbeitungs Anwendungen zum Abrufen und Anwenden von Verarbeitungseinstellungen Sitzungs übergreifend aktivieren.</span><span class="sxs-lookup"><span data-stu-id="eb065-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="eb065-113">Der Hauptzweck der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle besteht darin, Anwendungsentwicklern das Erstellen einer Benutzeroberfläche zum Anpassen von unformatierten Parametern zu ermöglichen, die so konsistent wie möglich über verschiedene Codecs hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="eb065-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="eb065-114">Angenommen, ein Endbenutzer passt die Parameter mit einem Schieberegler-Steuerelement an, wobei die minimalen und maximalen Werte dem minimalen und maximalen Bereich für den Parameter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="eb065-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="eb065-115">Um dies zu unterstützen, sollten Sie alle Parameterbereiche als linear behandeln.</span><span class="sxs-lookup"><span data-stu-id="eb065-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="eb065-116">Um sicherzustellen, dass die Schieberegler-Steuerelemente nicht übermäßig sensibel sind, sollten Sie auch so weit wie möglich einen Bereich für jeden Parameter unterstützen und dabei mindestens 50 Prozent des maximal möglichen Bereichs abdecken.</span><span class="sxs-lookup"><span data-stu-id="eb065-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="eb065-117">Beispiel: Wenn der maximal mögliche Kontrastbereich von "rein grau" zu "schwarz" und "weiß" ist, wobei der Standardwert "0,0" zugeordnet wird, würde der von einem Codec unterstützte Mindestbereich von mindestens Mitte zwischen dem Standardwert und dem reinen grauen am unteren Ende (– 1,0) liegen 1,0.</span><span class="sxs-lookup"><span data-stu-id="eb065-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


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



-   [<span data-ttu-id="eb065-118">Queryrawcapabilitiesinfo</span><span class="sxs-lookup"><span data-stu-id="eb065-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="eb065-119">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb065-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="eb065-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb065-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="eb065-121">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="eb065-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="eb065-122">Set/getcurrentparameterrgb, Set/GetNamedWhitePoint, Set/GetWhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="eb065-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="eb065-123">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="eb065-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="eb065-124">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="eb065-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="eb065-125">Set/getschärding</span><span class="sxs-lookup"><span data-stu-id="eb065-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="eb065-126">Set/getationations</span><span class="sxs-lookup"><span data-stu-id="eb065-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="eb065-127">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="eb065-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="eb065-128">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="eb065-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="eb065-129">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="eb065-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="eb065-130">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="eb065-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="eb065-131">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="eb065-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="eb065-132">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="eb065-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="eb065-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="eb065-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="eb065-134">Queryrawcapabilitiesinfo</span><span class="sxs-lookup"><span data-stu-id="eb065-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="eb065-135">[**Queryrawcapabilitiesinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) gibt den Satz unterstützter Funktionen für diese Rohdatendatei zurück.</span><span class="sxs-lookup"><span data-stu-id="eb065-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="eb065-136">Die [**wicrawcapabilitiesinfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="eb065-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


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



<span data-ttu-id="eb065-137">Die in dieser Struktur verwendete [**wicrawfunktionalitäten**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) -Enumeration wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="eb065-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="eb065-138">Das letzte Feld ist eine [**wicrawrotationfunktionalitäten**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) -Enumeration, die wie folgt definiert ist:</span><span class="sxs-lookup"><span data-stu-id="eb065-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="eb065-139">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb065-139">LoadParameterSet</span></span>

<span data-ttu-id="eb065-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) ermöglicht dem Benutzer, anzugeben, ob als Erstellungseinstellungen verwendet werden sollen, Benutzer angepasste Einstellungen verwendet oder der Decoder aufgefordert werden soll, das Bild automatisch zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="eb065-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="eb065-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb065-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="eb065-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) gibt ein **IPropertyBag2** mit dem aktuellen Parametersatz zurück.</span><span class="sxs-lookup"><span data-stu-id="eb065-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="eb065-143">Der Aufrufer kann dann diesen Parametersatz an den Encoder übergeben, der als Codierungsoptionen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb065-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="eb065-144">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="eb065-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="eb065-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) und [**eintexposurecompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) geben die auf die endgültige Ausgabe anzuwendende ausgabenkompensierung an.</span><span class="sxs-lookup"><span data-stu-id="eb065-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="eb065-146">Der gültige Bereich für EV ist – 5,0 bis + 5,0 Stopps.</span><span class="sxs-lookup"><span data-stu-id="eb065-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="eb065-147">Set/getcurrentparameterrgb, Set/GetNamedWhitePoint, Set/GetWhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="eb065-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="eb065-148">Diese Funktionen bieten alle Möglichkeiten zum Aufrufen und Festlegen des weißen Punkts, entweder als RGB-Wert, als vordefinierter benannter Wert oder als Kelvin-Wert.</span><span class="sxs-lookup"><span data-stu-id="eb065-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="eb065-149">Der zulässige Bereich für Kelvin ist 1.500 – 30.000.</span><span class="sxs-lookup"><span data-stu-id="eb065-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="eb065-150">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="eb065-150">Set/GetContrast</span></span>

<span data-ttu-id="eb065-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) und [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) geben den Kontrast an, der auf die Ausgabe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb065-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="eb065-152">Der gültige Bereich für die Angabe des Kontrasts ist – 1,0 bis + 1,0, wobei der Standard Kontrast 0,0 ist.</span><span class="sxs-lookup"><span data-stu-id="eb065-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="eb065-153">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="eb065-153">Set/GetGamma</span></span>

<span data-ttu-id="eb065-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) und [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) geben das anzuwendende Gamma an.</span><span class="sxs-lookup"><span data-stu-id="eb065-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="eb065-155">Der gültige Bereich für Gamma ist 0,2 bis 5,0, wobei 1,0 der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="eb065-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="eb065-156">Gamma wird in der Regel mit der herkömmlichen Gamma Power-Funktion implementiert (eine lineare Energie Funktion mit Unity-Gewinn).</span><span class="sxs-lookup"><span data-stu-id="eb065-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="eb065-157">Die Helligkeit wird mit zunehmender Gamma Steigerung erhöht und verringert, wenn Gamma den Wert 0 erreicht.</span><span class="sxs-lookup"><span data-stu-id="eb065-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="eb065-158">(Beachten Sie, dass der minimale Wert ungleich 0 (null) ist, weil NULL in herkömmlichen Gamma Berechnungen zu einem Fehler aufgrund einer Division durch Null führt.</span><span class="sxs-lookup"><span data-stu-id="eb065-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="eb065-159">Das logische Mindestlimit beträgt 1/Max, weshalb das Minimalwert 0,2 ist.)</span><span class="sxs-lookup"><span data-stu-id="eb065-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="eb065-160">Set/getschärding</span><span class="sxs-lookup"><span data-stu-id="eb065-160">Set/GetSharpness</span></span>

<span data-ttu-id="eb065-161">[**Getschärding**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) und [**setschärding**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) geben den Umfang der anzuwendenden Schärfe an.</span><span class="sxs-lookup"><span data-stu-id="eb065-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="eb065-162">Der gültige Bereich ist – 1,0 bis + 1,0, wobei 0,0 der Standardwert für die Schärfe ist, und – 1,0, was überhaupt keine Schärfe angibt.</span><span class="sxs-lookup"><span data-stu-id="eb065-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="eb065-163">Set/getationations</span><span class="sxs-lookup"><span data-stu-id="eb065-163">Set/GetSaturation</span></span>

<span data-ttu-id="eb065-164">" [**Getationations**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) " und "die fest [**legung**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) " geben den Umfang der anzuwendenden Sättigung an.</span><span class="sxs-lookup"><span data-stu-id="eb065-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="eb065-165">Der gültige Bereich zum Angeben der Sättigung ist – 1,0 bis + 1,0, wobei 0,0 eine normale Sättigung ist, – 1,0 die vollständige Überlastung darstellt, und + 1,0, die eine vollständige Sättigung darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb065-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="eb065-166">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="eb065-166">Set/GetTint</span></span>

<span data-ttu-id="eb065-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) und [**settint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) geben das anzuwendende Tönungs an, wenn ein grünes/Magenta-Bias angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb065-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="eb065-168">Der gültige Bereich liegt zwischen – 1,0 und + 1,0, wobei grün auf der negativen Seite der Skala und Magenta auf der positiven Seite liegt.</span><span class="sxs-lookup"><span data-stu-id="eb065-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="eb065-169">Die Tönungs-Skala ist als orthogonal bis Color-Temperatur definiert.</span><span class="sxs-lookup"><span data-stu-id="eb065-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="eb065-170">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="eb065-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="eb065-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) und [**setnoisereduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) geben die Menge der anzuwendenden Rauschunterdrückung an.</span><span class="sxs-lookup"><span data-stu-id="eb065-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="eb065-172">Der gültige Bereich für ist – 1,0 bis + 1,0.0,0 gibt die Standardmenge der Rauschunterdrückung an, – 1,0 bedeutet, dass keine Rauschunterdrückung erfolgt und + 1,0 eine maximale Rauschunterdrückung angibt.</span><span class="sxs-lookup"><span data-stu-id="eb065-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="eb065-173">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="eb065-173">SetDestinationColorContext</span></span>

<span data-ttu-id="eb065-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) gibt das Farbprofil an, das auf das Bild angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb065-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="eb065-175">Sie können [**getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) aufrufen, um das aktuelle Farbprofil abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb065-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="eb065-176">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="eb065-176">Set/GetToneCurve</span></span>

<span data-ttu-id="eb065-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) und [**settonecurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) geben Sie die anzuwendende Tonkurve an.</span><span class="sxs-lookup"><span data-stu-id="eb065-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="eb065-178">Angenommen, lineare Interpolationen zwischen Punkten.</span><span class="sxs-lookup"><span data-stu-id="eb065-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="eb065-179">**PToneCurve** ist eine [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) -Struktur, die ein Array aus [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) -Strukturen und eine Anzahl der Punkte im Array enthält.</span><span class="sxs-lookup"><span data-stu-id="eb065-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="eb065-180">Ein [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) enthält einen Eingabe Wert und einen Ausgabewert.</span><span class="sxs-lookup"><span data-stu-id="eb065-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="eb065-181">Wenn der Aufrufer **null** im *pToneCurve* -Parameter übergibt, sollten Sie die erforderliche Größe für die [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) im *pcbActualToneCurveBufferSize* -Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb065-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="eb065-182">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="eb065-182">Set/GetRotation</span></span>

<span data-ttu-id="eb065-183">" [**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) " und " [**ttrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) " geben den Grad der anzuwendenden Drehung an.</span><span class="sxs-lookup"><span data-stu-id="eb065-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="eb065-184">Eine Drehung von 90,0 würde eine Drehung von 90 Grad im Uhrzeigersinn angeben.</span><span class="sxs-lookup"><span data-stu-id="eb065-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="eb065-185">(Der Unterschied zwischen der Verwendung von "  **SetRotation** " und dem Festlegen der Drehung mithilfe der [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) -Methode besteht darin, dass der Drehungs Winkel, der mithilfe von " **SetRotation** " festgelegt wird, vom Codec beibehalten werden soll</span><span class="sxs-lookup"><span data-stu-id="eb065-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="eb065-186">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="eb065-186">Set/GetRenderMode</span></span>

<span data-ttu-id="eb065-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) und [**setrendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) geben die Qualität der Ausgabe an, die der Aufrufer benötigt.</span><span class="sxs-lookup"><span data-stu-id="eb065-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="eb065-188">Wenn ein Benutzerparameter anpasst, sollte die Anwendung eine sehr schnelle Näherung des tatsächlichen Bilds anzeigen, wenn die Änderungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb065-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="eb065-189">Zu diesem Zweck wird das Bild normalerweise bei der Bildschirmauflösung oder weniger angezeigt, anstatt bei der tatsächlichen Bildauflösung, um dem Benutzer sofortiges Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="eb065-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="eb065-190">Dies ist der Fall, wenn eine Anwendung die Qualität des Entwurfs Modus anfordern würde, sodass dies sehr schnell sein sollte.</span><span class="sxs-lookup"><span data-stu-id="eb065-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="eb065-191">Wenn der Benutzer alle Änderungen vorgenommen hat, Sie in der Vorschau im Entwurfs Modus angezeigt haben und sich entschieden haben, das vollständige Image mit den aktuellen Einstellungen zu decodieren, fordert die Anwendung einen Decodieren der optimalen Qualität an.</span><span class="sxs-lookup"><span data-stu-id="eb065-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="eb065-192">Dies wird in der Regel auch zum Drucken angefordert.</span><span class="sxs-lookup"><span data-stu-id="eb065-192">This is usually also requested for printing.</span></span> <span data-ttu-id="eb065-193">Wenn ein angemessener Kompromiss zwischen Geschwindigkeit und Qualität erforderlich ist, fordert die Anwendung die normale Qualität an.</span><span class="sxs-lookup"><span data-stu-id="eb065-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="eb065-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="eb065-194">SetNotificationCallback</span></span>

<span data-ttu-id="eb065-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registriert eine Rückruffunktion, die der Decoder aufruft, wenn sich einer der rohverarbeitungs Parameter ändert.</span><span class="sxs-lookup"><span data-stu-id="eb065-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="eb065-196">Die Signatur für [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) verfügt nur über eine Methode, die als " [**Benachrichtigen**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify)" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="eb065-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="eb065-197">**Notify** weist einen einzelnen Parameter auf, bei dem es sich um eine Maske handelt, die angibt, welche der rohverarbeitungs Parameter geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="eb065-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="eb065-198">Ein-oder-Vorgang wird für die folgenden Werte für die notificationmask ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb065-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="eb065-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb065-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="eb065-200">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="eb065-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb065-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="eb065-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="eb065-202">**Licher**</span><span class="sxs-lookup"><span data-stu-id="eb065-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb065-203">Implementieren von IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="eb065-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="eb065-204">Implementieren eines WIC-Enabled Encoders</span><span class="sxs-lookup"><span data-stu-id="eb065-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="eb065-205">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="eb065-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="eb065-206">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="eb065-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



