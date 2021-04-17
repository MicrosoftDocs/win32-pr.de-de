---
title: Text Dienst Registrierung
description: Zusätzlich zu den standardmäßigen com-in-proc Server-Registrierungs Einträgen muss sich ein Text Dienst selbst beim Text Services-Framework (TSF) registrieren, damit er für die Verwendung mit einer Anwendung verfügbar ist.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Dienst Framework (TSF), Registrierung
- TSF (Text Dienst Framework), Registrierung
- Text Dienste, Registrierung
- Text Dienst Framework (TSF), sprach profile
- TSF (Text Services Framework), sprach profile
- Text Dienste, sprach profile
- Text Dienst Framework (TSF), Kategorien
- TSF (Text Dienst Framework), Kategorien
- Text Dienste, Kategorien
- Registrieren von Text Diensten
- Registrieren von sprach Profilen
- Kategorien werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473628"
---
# <a name="text-service-registration"></a>Text Dienst Registrierung

Zusätzlich zu den standardmäßigen com-in-proc Server-Registrierungs Einträgen muss sich ein Text Dienst selbst beim Text Services-Framework (TSF) registrieren, damit er für die Verwendung mit einer Anwendung verfügbar ist. TSF stellt die Schnittstelle [itfinputprocessorprofiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) und [itfcategorymgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) bereit, um den Registrierungsprozess zu vereinfachen.

Text Dienstanbieter sollten auch digitale Signaturen mit Ihren binären ausführbaren Dateien bereitstellen. Siehe [Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="registering-the-text-service"></a>Registrieren des Text Dienstanbieter

Ein Text Dienst registriert sich bei TSF durch Aufrufen von [itfinputprocessorprofiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) mit dem Klassen Bezeichner des Text dienstanzdienstaners. Eine Instanz der **itfinputprocessorprofiles** -Schnittstelle wird durch Aufrufen von **CoCreateInstance** mit CLSID \_ tf \_ inputprocessorprofiles abgerufen.

Im folgenden Beispiel wird veranschaulicht, wie ein **itfinputprocessorprofiles** -Objekt erstellt und der Text Dienst registriert wird.


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[Itfinputprocessorprofiles:: Unregister](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>Registrieren von sprach Profilen

Ein Text Dienst ist nur verfügbar, wenn eine Anwendung den Fokus besitzt und in der sprach Leiste die richtige Sprache ausgewählt ist. Um dies zu vereinfachen, erfordert TSF, dass sich ein Text Dienst selbst für alle unterstützten Sprachen registriert. Der Text Dienst registriert seine sprach Profile durch Aufrufen von [itfinputprocessorprofiles:: addlanguageprofile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) mit dem Text Dienst-Klassen Bezeichner, dem sprach Bezeichner des Profils und einer durch den Text Dienst definierten **GUID** , die das Sprachprofil identifiziert.

Ein Sprachprofil kann durch Aufrufen von [itfinputprocessorprofiles:: removelanguageprofile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile)entfernt werden. **Itfinputprocessorprofiles:: unregister** entfernt alle sprach Profile für den Text Dienst. Wenn ein Text Dienst deinstalliert wird, müssen die einzelnen sprach Profile entfernt werden.

## <a name="registering-categories"></a>Kategorien werden registriert

Ein Text Dienst muss auch die Kategorie registrieren, für die der Text Dienst gilt. Wenn der Text Dienst beispielsweise Anzeige Attributinformationen liefert, muss er sich selbst als Anzeige Attribut Anbieter registrieren, indem [itfcategorymgr:: registercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassen Bezeichner des Text Dienstanbieters für den ersten Parameter, GUID \_ tfcat \_ displayattributeprovider für den zweiten Parameter und der Klassen Bezeichner des Text Dienstanbieters für den dritten Parameter. Die möglichen Kategorien sind unter [vordefinierte Kategoriewerte](predefined-category-values.md)aufgeführt.

Entfernen Sie zuvor registrierte Kategorien durch Aufrufen von [itfcategorymgr:: unregistercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory). Itfinputprocessorprofiles:: unregister entfernt alle Kategorien für den Text Dienst. Wenn ein Text Dienst deinstalliert wird, müssen die einzelnen Kategorien entfernt werden.

 

 