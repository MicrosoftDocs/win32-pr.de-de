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
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="ef997-103">Anpassen des mathematischen Eingabe Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef997-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="ef997-104">Es ist möglich, das Aussehen und das Gefühl des mathematischen Eingabe Steuer Elements zu ändern, damit es besser für Ihre Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ef997-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="ef997-105">In diesem Thema werden die verschiedenen Möglichkeiten erläutert, wie Entwickler das mathematische Eingabe Steuerelement anpassen können.</span><span class="sxs-lookup"><span data-stu-id="ef997-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="ef997-106">Die folgenden Anpassungen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ef997-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="ef997-107">Ändern der angezeigten Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="ef997-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="ef997-108">Ändern der Beschriftung des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef997-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="ef997-109">Ändern der Vorschau Bereichs Größe des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef997-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="ef997-110">Ändern der angezeigten Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="ef997-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="ef997-111">Sie können die Schaltflächen ändern, die auf dem mathematischen Eingabe Steuerelement angezeigt werden, damit das Steuerelement über erweiterte Funktionen verfügt oder auf dem Bildschirm kleiner erscheint.</span><span class="sxs-lookup"><span data-stu-id="ef997-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="ef997-112">Wenn Sie den erweiterten Schaltflächen Satz aktivieren, werden die Schaltflächen **Redo** und **Undo** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef997-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="ef997-113">Der folgende Code zeigt, wie Sie den erweiterten Schaltflächen Satz aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ef997-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="ef997-114">Die folgende Abbildung zeigt das-Steuerelement mit den erweiterten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="ef997-114">The following image shows the control with the extended set of buttons.</span></span>

![mathematisches Eingabe Steuerelement mit einem erweiterten Satz von Schaltflächen](images/mic.png)

<span data-ttu-id="ef997-116">Die folgende Abbildung zeigt das-Steuerelement ohne den erweiterten Satz von Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="ef997-116">The following image shows the control without the extended set of buttons.</span></span>

![mathematisches Eingabe Steuerelement ohne erweiterte Schaltflächen](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="ef997-118">Ändern der Beschriftung des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef997-118">Changing the Control Caption</span></span>

<span data-ttu-id="ef997-119">Sie können die Beschriftung des Steuer Elements für das mathematische Eingabe Steuerelement ändern, um die Beschriftung im Fenster des mathematischen Eingabe Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef997-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="ef997-120">Der folgende Code zeigt, wie die Beschriftung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ef997-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="ef997-121">Die folgende Abbildung zeigt das-Steuerelement, nachdem die Beschriftung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef997-121">The following image shows the control after the caption has been set.</span></span>

![mathematisches Eingabe Steuerelement mit einem Beschriftungs Satz](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="ef997-123">Ändern der Vorschau Bereichs Größe des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef997-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="ef997-124">Sie können das mathematische Eingabe Steuerelement so anpassen, dass das Steuerelement seine Vorschau Bereichs Größe explizit festlegt.</span><span class="sxs-lookup"><span data-stu-id="ef997-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="ef997-125">Dadurch wird ein größerer Bereich erstellt, in dem die mathematischen Formeln angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ef997-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="ef997-126">Der folgende Code zeigt, wie die Vorschau Bereichs Größe festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ef997-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="ef997-127">Die folgenden Bilder zeigen ein Steuerelement mit unterschiedlichen Vorschau Bereichen.</span><span class="sxs-lookup"><span data-stu-id="ef997-127">The following images show a control with differently sized preview areas.</span></span>

![mathematisches Eingabe Steuerelement mit der Standardgröße des Vorschau Bereichs](images/mic.png)![mathematisches Eingabe Steuerelement mit einem größeren Vorschaubereich](images/mic-big-preview.png)

 

 



