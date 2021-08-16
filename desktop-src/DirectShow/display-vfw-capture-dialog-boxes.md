---
description: Dialogfelder "VFW-Erfassung anzeigen"
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Dialogfelder "VFW-Erfassung anzeigen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2713cc4d2eba52626c66974eed23f2c1752a1268fea78a30ca2bc9d7babc3a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821138"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Dialogfelder "VFW-Erfassung anzeigen"

Ein Erfassungsgerät, das weiterhin einen VFW-Treiber (Video for Windows) verwendet, kann eines der folgenden drei Dialogfelder unterstützen, die zum Konfigurieren des Geräts verwendet werden.



| Dialogfeld    | BESCHREIBUNG                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Videoquelle  | Wird zum Auswählen der Videoeingabe und zum Anpassen von Geräteeinstellungen verwendet, z. B. Bildhelligkeit oder Kontrast. |
| Videoformat  | Wird verwendet, um die Bilddimensionen und die Bittiefe auszuwählen.                                                    |
| Videoanzeige | Wird verwendet, um die Darstellung des gerenderten Videos zu steuern.                                                 |



 

Um eines dieser Dialogfelder anzuzeigen, gehen Sie folgendermaßen vor:

1.  Beenden Sie das Filterdiagramm.
2.  Fragen Sie den Erfassungsfilter für die [**IAMVfwCaptureDialogs-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) ab. Wenn **QueryInterface** erfolgreich ist, bedeutet dies, dass das Erfassungsgerät ein VFW-Gerät ist.
3.  Rufen Sie [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) auf, um zu überprüfen, ob der Treiber das anzuzeigende Dialogfeld unterstützt. Die [**VfwCaptureDialogs-Enumeration**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) definiert Flags für jedes der VFW-Dialogfelder. **HasDialog** gibt S \_ OK zurück, wenn das Dialogfeld unterstützt wird. Andernfalls wird S FALSE zurückgegeben. Suchen Sie daher direkt nach \_ dem Wert S \_ OK, anstatt das **SUCCEEDED-Makro** zu verwenden.
4.  Wenn das Dialogfeld unterstützt wird, rufen [**Sie IAMVfwCaptureDialogs::ShowDialog auf,**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) um das Dialogfeld anzuzeigen.
5.  Starten Sie das Diagramm neu.

Der folgende Code zeigt diese Schritte für das Dialogfeld Videoquelle:


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

[Konfigurieren eines Videoaufnahmegeräts](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



