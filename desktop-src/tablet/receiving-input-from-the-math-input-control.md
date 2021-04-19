---
description: In diesem Abschnitt wird erläutert, wie das MathML-Markup mithilfe des Active Template Library (ATL) und des Component Object Model (com) aus dem mathematischen Eingabe Steuerelement abgerufen wird.
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Empfangen von Eingaben aus dem mathematischen Eingabe Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359521"
---
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="8d68e-103">Empfangen von Eingaben aus dem mathematischen Eingabe Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8d68e-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="8d68e-104">In diesem Abschnitt wird erläutert, wie das MathML-Markup mithilfe des Active Template Library (ATL) und des Component Object Model (com) aus dem mathematischen Eingabe Steuerelement abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8d68e-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="8d68e-105">Wenn Sie die erkannte mathematische Gleichung aus dem mathematischen Eingabe Steuerelement abrufen möchten, können Sie das Verhalten überschreiben, das beim Drücken der einfügeschaltfläche auftritt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="8d68e-106">Zu diesem Zweck müssen Sie einen Ereignishandler einrichten, der die verschiedenen Ereignisse implementiert, die von der [**\_ imathinputcontrolevents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) -Schnittstelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8d68e-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="8d68e-107">Das Einrichten des Ereignis Handlers umfasst die folgenden Schritte für die Ereignisse, die Sie unterstützen möchten (in diesem Fall einfügen).</span><span class="sxs-lookup"><span data-stu-id="8d68e-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="8d68e-108">Erstellen einer Vorlagen Klasse, die Ereignis senken enthält</span><span class="sxs-lookup"><span data-stu-id="8d68e-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="8d68e-109">Einrichten von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="8d68e-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="8d68e-110">Erben der Ereignishandlerklasse in der Hauptklasse</span><span class="sxs-lookup"><span data-stu-id="8d68e-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="8d68e-111">Initialisieren der Klasse zum Erben der Ereignis Senke (n)</span><span class="sxs-lookup"><span data-stu-id="8d68e-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="8d68e-112">Erstellen einer Vorlagen Klasse, die Ereignis senken enthält</span><span class="sxs-lookup"><span data-stu-id="8d68e-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="8d68e-113">Wenn Sie eine Ereignis Senke implementieren, die das mathematische Eingabe Steuerelement verwendet, müssen Sie zuerst eine Senke-ID angeben. Sie müssen dann eine Vorlagen Klasse erstellen, die von den Ereignis Schnittstellen Ereignis, Ereignis Steuerelement Handler und Math-Eingabesteuerung erbt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="8d68e-114">Der folgende Code zeigt, wie Sie eine Senke-ID festlegen und eine solche Vorlagen Klasse (cmathinputcontroleventhandler) erstellen, die von den erforderlichen Schnittstellen erbt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="8d68e-115">Diese Vorlagen Klasse ist auch so eingerichtet, dass Sie über einen privaten unbekannten Schnittstellen Zeiger verfügt, der verwendet wird, um das mathematische Eingabe Steuerelement bei der Initialisierung an das Steuerelement zu übergeben, und das m \_ uladvisecount-Element, um die Anzahl der Aufrufe für "Empfehlung/nicht Empfehlung" zu</span><span class="sxs-lookup"><span data-stu-id="8d68e-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> <span data-ttu-id="8d68e-116">Der Member **m \_ pmain** sollte in ihrer Implementierung anders sein, wenn Sie kein Dialogfeld verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d68e-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="8d68e-117">Nachdem Sie nun über die grundlegende Vorlagen Klasse verfügen, müssen Sie eine vorwärts Deklaration für die Ereignishandler, die Sie überschreiben, erstellen und dann eine senkenzuordnung für die Ereignisse einrichten, die Sie behandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="8d68e-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="8d68e-118">Der folgende Code zeigt, wie Sie Ereignishandler für die [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) -Methode einrichten, die aufgerufen wird, wenn ein Benutzer auf die Schaltfläche Einfügen im math-Eingabe Steuerelement klickt, und die [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) -Methode, die aufgerufen wird, wenn ein Benutzer auf die Schaltfläche Abbrechen im math-Eingabe Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="8d68e-119">Da Sie mit dem mathematischen Eingabe Steuerelement arbeiten werden, ist es hilfreich, einen internen Verweis auf die relevante Schnittstelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8d68e-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="8d68e-120">Die folgende Utility-Funktion wird in der Beispiel Klasse erstellt, um diesen Verweis festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8d68e-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="8d68e-121">Einrichten von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="8d68e-121">Set up the event handlers</span></span>

<span data-ttu-id="8d68e-122">Nachdem Sie die Ereignis senken eingerichtet haben, müssen Sie Ihre Implementierungen der Ereignis senken erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d68e-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="8d68e-123">In beiden Methoden im folgenden Codebeispiel rufen die Ereignis senken ein Handle für die mathematische Eingabe Steuerungs Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="8d68e-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="8d68e-124">In der [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) -Funktion wird das Erkennungs Ergebnis als MathML angezeigt, und das-Steuerelement ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8d68e-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="8d68e-125">In der [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) -Funktion wird das mathematische Eingabe Steuerelement ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8d68e-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="8d68e-126">Erben der Ereignishandlerklasse in der Hauptklasse</span><span class="sxs-lookup"><span data-stu-id="8d68e-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="8d68e-127">Nachdem Sie die Vorlagen Klasse implementiert haben, müssen Sie Sie in der Klasse erben, in der Sie Ihr mathematisches Eingabe Steuerelement einrichten werden.</span><span class="sxs-lookup"><span data-stu-id="8d68e-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="8d68e-128">Im Rahmen dieses Handbuchs ist diese Klasse ein Dialogfeld, CMIC \_ Test \_ eventsdlg.</span><span class="sxs-lookup"><span data-stu-id="8d68e-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="8d68e-129">Im Dialog Header müssen die erforderlichen Header eingeschlossen werden, und die von Ihnen erstellte Vorlagen Klasse muss geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="8d68e-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="8d68e-130">Die Klasse, die Sie in und den Ereignis Handlern erbt, muss über vorwärts Deklarationen verfügen, damit die Vorlage implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d68e-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="8d68e-131">Das folgende Codebeispiel zeigt, wie dies geschieht.</span><span class="sxs-lookup"><span data-stu-id="8d68e-131">The following code example shows how this is done.</span></span>


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> <span data-ttu-id="8d68e-132">Der Vorlagentyp **CMIC \_ Test \_ eventsdlg** ist anders, es sei denn, Sie haben die Klasse mit dem Beispiel benannt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="8d68e-133">Initialisieren der Klasse zum Erben der Ereignis Senke (n)</span><span class="sxs-lookup"><span data-stu-id="8d68e-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="8d68e-134">Nachdem Sie Ihre Klasse so eingerichtet haben, dass Sie von der Vorlagen Klasse geerbt wird, können Sie Sie zum Behandeln von Ereignissen einrichten.</span><span class="sxs-lookup"><span data-stu-id="8d68e-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="8d68e-135">Dies besteht aus der Initialisierung der-Klasse, um ein Handle für das mathematische Eingabe Steuerelement und die aufrufenden Klasse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d68e-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="8d68e-136">Darüber hinaus muss das mathematische Eingabe Steuerelement zum Verarbeiten von Ereignissen von an die dispeventclaim-Methode gesendet werden, die die cmathinputcontroleventhandler-Beispiel Klasse erbt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="8d68e-137">Der folgende Code wird von der OnInitDialog-Methode in der Example-Klasse aufgerufen, um diese Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d68e-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> <span data-ttu-id="8d68e-138">Der Vorlagentyp CMIC \_ Test \_ eventsdlg in diesem Beispiel ist anders, es sei denn, Sie haben die Klasse mit dem Beispiel identisch benannt.</span><span class="sxs-lookup"><span data-stu-id="8d68e-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
