---
description: Erläutert, wie die Darstellung des mathematischen Eingabe Steuer Elements geändert wird.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Anpassen des mathematischen Eingabe Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567731"
---
# <a name="customizing-the-math-input-control"></a>Anpassen des mathematischen Eingabe Steuer Elements

Es ist möglich, das Aussehen und das Gefühl des mathematischen Eingabe Steuer Elements zu ändern, damit es besser für Ihre Anwendung geeignet ist. In diesem Thema werden die verschiedenen Möglichkeiten erläutert, wie Entwickler das mathematische Eingabe Steuerelement anpassen können.

Die folgenden Anpassungen sind möglich:

-   [Ändern der angezeigten Schaltflächen](#changing-the-displayed-buttons)
-   [Ändern der Beschriftung des Steuer Elements](#changing-the-control-caption)
-   [Ändern der Vorschau Bereichs Größe des Steuer Elements](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Ändern der angezeigten Schaltflächen

Sie können die Schaltflächen ändern, die auf dem mathematischen Eingabe Steuerelement angezeigt werden, damit das Steuerelement über erweiterte Funktionen verfügt oder auf dem Bildschirm kleiner erscheint. Wenn Sie den erweiterten Schaltflächen Satz aktivieren, werden die Schaltflächen **Redo** und **Undo** angezeigt. Der folgende Code zeigt, wie Sie den erweiterten Schaltflächen Satz aktivieren.


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



Die folgende Abbildung zeigt das-Steuerelement mit den erweiterten Schaltflächen.

![mathematisches Eingabe Steuerelement mit einem erweiterten Satz von Schaltflächen](images/mic.png)

Die folgende Abbildung zeigt das-Steuerelement ohne den erweiterten Satz von Schaltflächen.

![mathematisches Eingabe Steuerelement ohne erweiterte Schaltflächen](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Ändern der Beschriftung des Steuer Elements

Sie können die Beschriftung des Steuer Elements für das mathematische Eingabe Steuerelement ändern, um die Beschriftung im Fenster des mathematischen Eingabe Steuer Elements festzulegen. Der folgende Code zeigt, wie die Beschriftung festgelegt wird.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



Die folgende Abbildung zeigt das-Steuerelement, nachdem die Beschriftung festgelegt wurde.

![mathematisches Eingabe Steuerelement mit einem Beschriftungs Satz](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Ändern der Vorschau Bereichs Größe des Steuer Elements

Sie können das mathematische Eingabe Steuerelement so anpassen, dass das Steuerelement seine Vorschau Bereichs Größe explizit festlegt. Dadurch wird ein größerer Bereich erstellt, in dem die mathematischen Formeln angezeigt werden. Der folgende Code zeigt, wie die Vorschau Bereichs Größe festgelegt wird.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



Die folgenden Bilder zeigen ein Steuerelement mit unterschiedlichen Vorschau Bereichen.

![mathematisches Eingabe Steuerelement mit der Standardgröße des Vorschau Bereichs](images/mic.png)![mathematisches Eingabe Steuerelement mit einem größeren Vorschaubereich](images/mic-big-preview.png)

 

 



