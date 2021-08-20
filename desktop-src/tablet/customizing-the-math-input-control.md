---
description: Erläutert, wie die Darstellung des mathematischen Eingabesteuerfelds geändert wird.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Anpassen der Steuerung für mathematische Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adedc4ab5b655f4f753a1b83cabe28e322adaad3c73bcf9f25ea1dea6d0bc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045641"
---
# <a name="customizing-the-math-input-control"></a>Anpassen der Steuerung für mathematische Eingaben

Es ist möglich, das Aussehen und Aussehen des mathematischen Eingabesteuerfelds so zu ändern, dass es besser für Ihre Anwendung geeignet ist. In diesem Thema werden die verschiedenen Möglichkeiten erläutert, wie Entwickler das steuerelement für mathematische Eingaben anpassen können.

Die folgenden Anpassungen sind möglich:

-   [Ändern der angezeigten Schaltflächen](#changing-the-displayed-buttons)
-   [Ändern der Steuerelementbeschriftung](#changing-the-control-caption)
-   [Ändern der Größe des Vorschaubereichs des Steuerelements](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Ändern der angezeigten Schaltflächen

Sie können die Schaltflächen ändern, die auf dem mathematischen Eingabesteuerfeld angezeigt werden, sodass das Steuerelement über erweiterte Funktionen verfügt oder kleiner auf dem Bildschirm angezeigt wird. Wenn Sie den erweiterten Schaltflächensatz aktivieren, werden die **Schaltflächen Wiederholen** und **Rückgängig** angezeigt. Der folgende Code zeigt, wie Sie den erweiterten Schaltflächensatz aktivieren.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



Die folgende Abbildung zeigt das Steuerelement mit dem erweiterten Satz von Schaltflächen.

![Mathematisches Eingabesteuerfeld mit einem erweiterten Satz von Schaltflächen](images/mic.png)

Die folgende Abbildung zeigt das Steuerelement ohne den erweiterten Satz von Schaltflächen.

![Mathematisches Eingabesteuerfeld ohne erweiterten Satz von Schaltflächen](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Ändern der Steuerelementbeschriftung

Sie können die Beschriftung des Steuerelements für die mathematische Eingabe ändern, um die Beschriftung im Fenster des Matheeingabe-Steuerelements zu festlegen. Der folgende Code zeigt, wie die Beschriftung festgelegt wird.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



Die folgende Abbildung zeigt das -Steuerelement, nachdem die Beschriftung festgelegt wurde.

![Mathematisches Eingabesteuerfeld mit einem Beschriftungssatz](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Ändern der Größe des Vorschaubereichs des Steuerelements

Sie können das mathematische Eingabesteuerfeld so anpassen, dass das Steuerelement die Größe des Vorschaubereichs explizit fest legt. Dadurch wird ein größerer Bereich erstellt, in dem die mathematischen Formeln angezeigt werden. Der folgende Code zeigt, wie sie die Größe des Vorschaubereichs festlegen.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



Die folgenden Abbildungen zeigen ein Steuerelement mit unterschiedlich großen Vorschaubereichen.

![Mathematisches Eingabesteuerfeld mit der Standardvorschaubereichsgröße](images/mic.png)![Mathematisches Eingabesteuerfeld mit einem größeren Vorschaubereich](images/mic-big-preview.png)

 

 



