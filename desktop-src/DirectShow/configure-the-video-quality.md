---
description: In diesem Thema wird beschrieben, wie eine Anwendung die Bild- und Kameraeinstellungen auf einem Videoaufnahmegerät programmgesteuert ändern kann.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Konfigurieren der Videoqualität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5987352eb329410efd3fc74d6bf12539e968da8e24d2f0a65af9c9ac7b5cb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871770"
---
# <a name="configure-the-video-quality"></a>Konfigurieren der Videoqualität

In diesem Thema wird beschrieben, wie eine Anwendung die Bild- und Kameraeinstellungen auf einem Videoaufnahmegerät programmgesteuert ändern kann.

-   [ProcAmp Einstellungen](#procamp-settings)
-   [Kameraeinstellungen](#camera-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="procamp-settings"></a>ProcAmp Einstellungen

Windows Videokameras des Treibermodells (Driver Model, WDM) können Eigenschaften unterstützen, die die Qualität des Bilds steuern:

-   Hintergrundbeleuchtungskompensierung
-   Brightness
-   Vergleichen Sie
-   Gewinnen
-   Gamma
-   Farbton
-   Sättigung
-   Schärfe
-   Weißabgleich

Diese Eigenschaften werden über die [**IAMVideoProcAmp-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) gesteuert. Verwenden Sie diese Schnittstelle wie folgt:

1.  Rufen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Erfassungsfilter für die [**IAMVideoProcAmp-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) auf.
2.  Rufen Sie für jede Eigenschaft, die Sie festlegen möchten, die [**IAMVideoProcAmp::GetRange-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) auf. Eigenschaften werden von der [**VideoProcAmpProperty-Enumeration**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) angegeben. Wenn die **GetRange-Methode** fehlschlägt, bedeutet dies, dass die Kamera diese bestimmte Eigenschaft nicht unterstützt.
3.  Wenn [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) erfolgreich ist, wird der Bereich der unterstützten Werte für die -Eigenschaft, der Standardwert und das minimale Inkrement zurückgegeben.
4.  Rufen Sie [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get)auf, um den aktuellen Wert einer Eigenschaft abzurufen.
5.  Um eine Eigenschaft festzulegen, rufen Sie die [**IAMVideoProcAmp::Set-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) auf. Um eine Eigenschaft auf ihren Standardwert wiederherzustellen, rufen [**Sie GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) auf, um den Standardwert zu suchen und diesen Wert an die **Set-Methode** zu übergeben.

Sie müssen das Filterdiagramm nicht beenden, wenn Sie die Eigenschaften festlegen.

Der folgende Code konfiguriert ein Trackbar-Steuerelement, sodass es zum Festlegen der Helligkeit verwendet werden kann. Der Bereich der Trackleiste entspricht dem Helligkeitsbereich, den das Gerät unterstützt, und die Position der Trackleiste entspricht der anfänglichen Helligkeitseinstellung des Geräts.


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

Die [**IAMCameraControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) ähnelt [**IAMVideoProcAmp,**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)steuert jedoch verschiedene Einstellungen für die Kamera selbst:

-   Belichtung
-   Fokus
-   Iris
-   Schwenken
-   rollen
-   Tilt
-   Zoom

Führen Sie die gleichen Schritte für [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)aus, um diese Schnittstelle zu verwenden:

1.  Fragen Sie den Erfassungsfilter für [**IAMCameraControl ab.**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)
2.  Rufen Sie [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) auf, um die unterstützten Einstellungen und den möglichen Bereich für die einzelnen Einstellungen zu ermitteln.
3.  Rufen Sie [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) auf, um den aktuellen Wert einer Einstellung abzurufen.
4.  Rufen Sie [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) auf, um den Wert festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren eines Videoaufnahmegeräts](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
