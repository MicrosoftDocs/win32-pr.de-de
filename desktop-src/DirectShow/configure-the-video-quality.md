---
description: In diesem Thema wird beschrieben, wie eine Anwendung das Bild und die Kameraeinstellungen auf einem Video Erfassungsgerät Programm gesteuert ändern kann.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Konfigurieren der Video Qualität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746056"
---
# <a name="configure-the-video-quality"></a>Konfigurieren der Video Qualität

In diesem Thema wird beschrieben, wie eine Anwendung das Bild und die Kameraeinstellungen auf einem Video Erfassungsgerät Programm gesteuert ändern kann.

-   [ProcAmp-Einstellungen](#procamp-settings)
-   [Kameraeinstellungen](#camera-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="procamp-settings"></a>ProcAmp-Einstellungen

WDM-Videokameras (Windows-Treibermodell) können Eigenschaften unterstützen, die die Qualität des Bilds Steuern:

-   Backlight-Kompensierung
-   Brightness
-   Vergleichen Sie
-   Erzielen
-   Gamma
-   Farbton
-   Sättigung
-   Schärfe
-   Weißabgleich

Diese Eigenschaften werden über die [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) -Schnittstelle gesteuert. Verwenden Sie diese Schnittstelle wie folgt:

1.  Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Erfassungs Filter für die [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) -Schnittstelle.
2.  Aufrufen Sie für jede Eigenschaft, die Sie festlegen möchten, die [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) -Methode. Eigenschaften werden von der [**videoprocampproperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) -Enumeration angegeben. Wenn die **GetRange** -Methode fehlschlägt, bedeutet dies, dass die Kamera diese bestimmte Eigenschaft nicht unterstützt.
3.  Wenn [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) erfolgreich ist, wird der Bereich der unterstützten Werte für die Eigenschaft, den Standardwert und das minimale Inkrement zurückgegeben.
4.  Um den aktuellen Wert einer Eigenschaft abzurufen, nennen Sie [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Um eine Eigenschaft festzulegen, müssen Sie die [**IAMVideoProcAmp:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) -Methode aufrufen. Um eine Eigenschaft auf ihren Standardwert wiederherzustellen, müssen Sie [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) aufrufen, um den Standardwert zu ermitteln und diesen Wert an die **set** -Methode zu übergeben.

Sie müssen das Filter Diagramm nicht beenden, wenn Sie die Eigenschaften festlegen.

Mit dem folgenden Code wird ein TrackBar-Steuerelement so konfiguriert, dass es zum Festlegen der Helligkeit verwendet werden kann. Der Bereich der TrackBar entspricht dem Gültigkeitsbereich, der vom Gerät unterstützt wird, und die Position der TrackBar entspricht der Einstellung für die anfängliche Helligkeit des Geräts.


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a>Kameraeinstellungen

Die [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) -Schnittstelle ähnelt [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), steuert jedoch verschiedene Einstellungen auf der Kamera selbst:

-   Belichtung
-   Fokus
-   Iris
-   Schwenken
-   N
-   Til
-   Zoom

Um diese Schnittstelle zu verwenden, führen Sie dieselben Schritte aus, die für [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)verwendet werden:

1.  Fragen Sie den Erfassungs Filter nach [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)ab.
2.  Aufrufen von [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) , um zu ermitteln, welche Einstellungen unterstützt werden, und den möglichen Bereich für jede Einstellung.
3.  Ruft [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) auf, um den aktuellen Wert einer Einstellung zu erhalten.
4.  Nennen Sie [**IAMCameraControl:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) , um den Wert festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren eines Video Erfassungs Geräts](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
