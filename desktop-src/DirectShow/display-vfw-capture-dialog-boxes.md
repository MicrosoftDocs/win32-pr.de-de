---
description: Dialog Felder zur VFW-Erfassung anzeigen
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Dialog Felder zur VFW-Erfassung anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745649"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Dialog Felder zur VFW-Erfassung anzeigen

Ein Erfassungsgerät, das weiterhin einen VFW-Treiber (Video for Windows) verwendet, kann eines der folgenden drei Dialogfelder unterstützen, die zum Konfigurieren des Geräts verwendet werden.



| Dialogfeld    | BESCHREIBUNG                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Video Quelle  | Wird verwendet, um die Videoeingabe auszuwählen und Geräteeinstellungen wie Bildhelligkeit oder Kontrast anzupassen. |
| Video Format  | Wird verwendet, um die Bild Dimensionen und die Bittiefe auszuwählen.                                                    |
| Video Anzeige | Wird verwendet, um die Darstellung des gerenderten Videos zu steuern.                                                 |



 

Gehen Sie folgendermaßen vor, um eines dieser Dialogfelder anzuzeigen:

1.  Stoppt das Filter Diagramm.
2.  Fragen Sie den Erfassungs Filter nach der [**iamvfwcapturedialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) -Schnittstelle ab. Wenn **QueryInterface** erfolgreich ist, bedeutet dies, dass das Erfassungsgerät ein VFW-Gerät ist.
3.  Aufrufen von [**iamvfwcapturedialoge:: hasdialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) zum Überprüfen, ob der Treiber das Dialogfeld unterstützt, das Sie anzeigen möchten. Die [**vfwcapturedialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) -Enumeration definiert Flags für jedes der Vfw-Dialogfelder. **Hasdialog** gibt S \_ OK zurück, wenn das Dialogfeld unterstützt wird. Andernfalls wird ' false ' zurückgegeben \_ . Überprüfen Sie, ob der Wert ' ' \_ OK ist, anstatt das Makro ' **erfolgreich** ' zu verwenden.
4.  Wenn das Dialogfeld unterstützt wird, müssen Sie [**iamvfwcapturedialoge:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) aufrufen, um das Dialogfeld anzuzeigen.
5.  Starten Sie das Diagramm neu.

Der folgende Code zeigt die folgenden Schritte für das Dialogfeld Video Quelle:


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren eines Video Erfassungs Geräts](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



