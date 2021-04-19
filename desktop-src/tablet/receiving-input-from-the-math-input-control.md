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
# <a name="receiving-input-from-the-math-input-control"></a>Empfangen von Eingaben aus dem mathematischen Eingabe Steuerelement

In diesem Abschnitt wird erläutert, wie das MathML-Markup mithilfe des Active Template Library (ATL) und des Component Object Model (com) aus dem mathematischen Eingabe Steuerelement abgerufen wird.

Wenn Sie die erkannte mathematische Gleichung aus dem mathematischen Eingabe Steuerelement abrufen möchten, können Sie das Verhalten überschreiben, das beim Drücken der einfügeschaltfläche auftritt. Zu diesem Zweck müssen Sie einen Ereignishandler einrichten, der die verschiedenen Ereignisse implementiert, die von der [**\_ imathinputcontrolevents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) -Schnittstelle unterstützt werden. Das Einrichten des Ereignis Handlers umfasst die folgenden Schritte für die Ereignisse, die Sie unterstützen möchten (in diesem Fall einfügen).

-   [Erstellen einer Vorlagen Klasse, die Ereignis senken enthält](#create-a-template-class-that-contains-event-sinks)
-   [Einrichten von Ereignis Handlern](#set-up-the-event-handlers)
-   [Erben der Ereignishandlerklasse in der Hauptklasse](#inherit-the-event-handler-class-in-your-main-class)
-   [Initialisieren der Klasse zum Erben der Ereignis Senke (n)](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Erstellen einer Vorlagen Klasse, die Ereignis senken enthält

Wenn Sie eine Ereignis Senke implementieren, die das mathematische Eingabe Steuerelement verwendet, müssen Sie zuerst eine Senke-ID angeben. Sie müssen dann eine Vorlagen Klasse erstellen, die von den Ereignis Schnittstellen Ereignis, Ereignis Steuerelement Handler und Math-Eingabesteuerung erbt. Der folgende Code zeigt, wie Sie eine Senke-ID festlegen und eine solche Vorlagen Klasse (cmathinputcontroleventhandler) erstellen, die von den erforderlichen Schnittstellen erbt. Diese Vorlagen Klasse ist auch so eingerichtet, dass Sie über einen privaten unbekannten Schnittstellen Zeiger verfügt, der verwendet wird, um das mathematische Eingabe Steuerelement bei der Initialisierung an das Steuerelement zu übergeben, und das m \_ uladvisecount-Element, um die Anzahl der Aufrufe für "Empfehlung/nicht Empfehlung" zu


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
> Der Member **m \_ pmain** sollte in ihrer Implementierung anders sein, wenn Sie kein Dialogfeld verwenden.

 

Nachdem Sie nun über die grundlegende Vorlagen Klasse verfügen, müssen Sie eine vorwärts Deklaration für die Ereignishandler, die Sie überschreiben, erstellen und dann eine senkenzuordnung für die Ereignisse einrichten, die Sie behandeln möchten. Der folgende Code zeigt, wie Sie Ereignishandler für die [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) -Methode einrichten, die aufgerufen wird, wenn ein Benutzer auf die Schaltfläche Einfügen im math-Eingabe Steuerelement klickt, und die [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) -Methode, die aufgerufen wird, wenn ein Benutzer auf die Schaltfläche Abbrechen im math-Eingabe Steuerelement klickt.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Da Sie mit dem mathematischen Eingabe Steuerelement arbeiten werden, ist es hilfreich, einen internen Verweis auf die relevante Schnittstelle festzulegen. Die folgende Utility-Funktion wird in der Beispiel Klasse erstellt, um diesen Verweis festzulegen.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Einrichten von Ereignis Handlern

Nachdem Sie die Ereignis senken eingerichtet haben, müssen Sie Ihre Implementierungen der Ereignis senken erstellen. In beiden Methoden im folgenden Codebeispiel rufen die Ereignis senken ein Handle für die mathematische Eingabe Steuerungs Schnittstelle ab. In der [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) -Funktion wird das Erkennungs Ergebnis als MathML angezeigt, und das-Steuerelement ist ausgeblendet. In der [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) -Funktion wird das mathematische Eingabe Steuerelement ausgeblendet.


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



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Erben der Ereignishandlerklasse in der Hauptklasse

Nachdem Sie die Vorlagen Klasse implementiert haben, müssen Sie Sie in der Klasse erben, in der Sie Ihr mathematisches Eingabe Steuerelement einrichten werden. Im Rahmen dieses Handbuchs ist diese Klasse ein Dialogfeld, CMIC \_ Test \_ eventsdlg. Im Dialog Header müssen die erforderlichen Header eingeschlossen werden, und die von Ihnen erstellte Vorlagen Klasse muss geerbt werden. Die Klasse, die Sie in und den Ereignis Handlern erbt, muss über vorwärts Deklarationen verfügen, damit die Vorlage implementiert werden kann. Das folgende Codebeispiel zeigt, wie dies geschieht.


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
> Der Vorlagentyp **CMIC \_ Test \_ eventsdlg** ist anders, es sei denn, Sie haben die Klasse mit dem Beispiel benannt.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Initialisieren der Klasse zum Erben der Ereignis Senke (n)

Nachdem Sie Ihre Klasse so eingerichtet haben, dass Sie von der Vorlagen Klasse geerbt wird, können Sie Sie zum Behandeln von Ereignissen einrichten. Dies besteht aus der Initialisierung der-Klasse, um ein Handle für das mathematische Eingabe Steuerelement und die aufrufenden Klasse zu erhalten. Darüber hinaus muss das mathematische Eingabe Steuerelement zum Verarbeiten von Ereignissen von an die dispeventclaim-Methode gesendet werden, die die cmathinputcontroleventhandler-Beispiel Klasse erbt. Der folgende Code wird von der OnInitDialog-Methode in der Example-Klasse aufgerufen, um diese Aktionen auszuführen.


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
> Der Vorlagentyp CMIC \_ Test \_ eventsdlg in diesem Beispiel ist anders, es sei denn, Sie haben die Klasse mit dem Beispiel identisch benannt.

 

 

 
