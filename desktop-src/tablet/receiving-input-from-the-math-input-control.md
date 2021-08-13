---
description: In diesem Abschnitt wird erläutert, wie Sie das MathML-Markup aus dem mathematischen Eingabesteuerfeld mithilfe des Active Template Library (ATL) und des Component Object Model (COM) abrufen.
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Empfangen von Eingaben vom Steuerung für mathematische Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50325b8e9980907b91f4cd6400ed6cfd0ef3f04367a2bc753e5d4065e189bc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449330"
---
# <a name="receiving-input-from-the-math-input-control"></a>Empfangen von Eingaben vom Steuerung für mathematische Eingaben

In diesem Abschnitt wird erläutert, wie Sie das MathML-Markup aus dem mathematischen Eingabesteuerfeld mithilfe des Active Template Library (ATL) und des Component Object Model (COM) abrufen.

Um die erkannte mathematische Gleichung aus dem mathematischen Eingabesteuerfeld abzurufen, können Sie das Verhalten überschreiben, das beim Drücken der Einfügeschaltfläche eintritt. Hierzu müssen Sie einen Ereignishandler einrichten, der die verschiedenen Ereignisse implementiert, die von der [**\_ IMathInputControlEvents-Schnittstelle unterstützt**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) werden. Das Einrichten des Ereignishandlers umfasst das Ausführen der folgenden Schritte für die Ereignisse, die Sie unterstützen möchten (in diesem Fall einfügen).

-   [Erstellen einer Vorlagenklasse, die Ereignissenken enthält](#create-a-template-class-that-contains-event-sinks)
-   [Einrichten der Ereignishandler](#set-up-the-event-handlers)
-   [Erben der Ereignishandlerklasse in der Hauptklasse](#inherit-the-event-handler-class-in-your-main-class)
-   [Initialisieren der Klasse zum Erben der Ereignissenken](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Erstellen einer Vorlagenklasse, die Ereignissenken enthält

Wenn Sie eine Ereignissenke implementieren, die das mathematische Eingabesteuerfeld verwendet, müssen Sie zunächst eine Senken-ID angeben. Anschließend müssen Sie eine Vorlagenklasse erstellen, die von den Ereignisschnittstellen ereignis, ereignissteuerhandler und math input control erbt. Der folgende Code zeigt, wie Sie eine Senken-ID festlegen und eine solche Vorlagenklasse( CMathInputControlEventHandler) erstellen, die von den erforderlichen Schnittstellen erbt. Diese Vorlagenklasse ist auch so eingerichtet, dass sie einen privaten unbekannten Schnittstellenzeiger hat, der verwendet wird, um das mathematische Eingabesteuerfeld bei der Initialisierung an sie zu übergeben, und das m ulAdviseCount-Member, um die Anzahl der Aufrufe zu zählen, die \_ "advise/unadvise" sind.


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
> Der Member **m \_ pMain sollte** sich in Ihrer Implementierung unterscheiden, wenn Sie kein Dialogfeld verwenden.

 

Da Sie nun über die grundlegende Vorlagenklasse verfügen, müssen Sie eine Vorwärtsdeklaration für die Ereignishandler geben, die Sie überschreiben werden, und dann eine Senkenzuordnung für die Ereignisse einrichten, die Sie behandeln. Der folgende Code zeigt, wie Ereignishandler für die [**Insert-Methode**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) eingerichtet werden, die aufgerufen wird, wenn ein Benutzer auf die Einfügeschaltfläche des mathematischen Eingabesteuerfelds klickt, und die [**Close-Methode,**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) die aufgerufen wird, wenn ein Benutzer auf die Schaltfläche "Abbrechen" im mathematischen Eingabesteuerfeld klickt.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Da Sie mit dem mathematischen Eingabesteuerfeld arbeiten, ist es hilfreich, einen internen Verweis auf die relevante Schnittstelle zu setzen. Die folgende Hilfsprogrammfunktion wird in der Beispielklasse erstellt, um diesen Verweis zu setzen.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Einrichten der Ereignishandler

Nachdem Sie die Ereignissenken eingerichtet haben, müssen Sie Ihre Implementierungen der Ereignissenken erstellen. In beiden Methoden im folgenden Codebeispiel rufen die Ereignissenken ein Handle für die Mathematische Eingabesteuerschnittstelle ab. In der [**Insert-Funktion**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) wird das Erkennungsergebnis als MathML angezeigt, und das Steuerelement ist ausgeblendet. In der [**Close-Funktion**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) ist das mathematische Eingabesteuerfeld ausgeblendet.


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

Nachdem Sie Ihre Vorlagenklasse implementiert haben, müssen Sie sie in die Klasse erben, in der Sie Ihr mathematisches Eingabesteuerfeld einrichten. Im Rahmen dieses Leitfadens ist diese Klasse ein Dialog, CMIC \_ TEST \_ EVENTSDlg. Im Dialogheader müssen die erforderlichen Header enthalten sein, und die von Ihnen erstellte Vorlagenklasse muss geerbt werden. Die Klasse, in der Sie erben, und die Ereignishandler müssen Vorwärtsdeklarationen haben, damit die Vorlage implementiert werden kann. Das folgende Codebeispiel zeigt, wie dies erfolgt.


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
> Der Vorlagentyp **CMIC \_ TEST \_ EventsDlg** ist anders, es sei denn, Sie haben Ihre Klasse wie im Beispiel benannt.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Initialisieren der Klasse zum Erben der Ereignissenken

Nachdem Sie ihre Klasse so eingerichtet haben, dass sie von der Vorlagenklasse erbt, können Sie sie für die Handhabung von Ereignissen einrichten. Dies besteht aus der Initialisierung der -Klasse, um ein Handle für das mathematische Eingabesteuerfeld und die aufrufende Klasse zu erhalten. Darüber hinaus muss das mathematische Eingabesteuerfeld zum Behandeln von Ereignissen von an die DispEventAdvise-Methode gesendet werden, die von der CMathInputControlEventHandler-Beispielklasse geerbt wird. Der folgende Code wird von der OnInitDialog-Methode in der Beispielklasse aufgerufen, um diese Aktionen durchzuführen.


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
> Der Vorlagentyp CMIC TEST EventsDlg in diesem Beispiel ist anders, es sei denn, Sie haben Ihre Klasse wie \_ \_ im Beispiel benannt.

 

 

 
