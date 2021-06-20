---
description: Definieren Sie einen Mechanismus zum Festlegen der Eigenschaft als Teil der Erstellung einer Filtereigenschaftsseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 'Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410073"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft

Der Filter muss eine Möglichkeit unterstützen, damit die Eigenschaftenseite damit kommunizieren kann, damit die Eigenschaftenseite Eigenschaften für den Filter festlegen und abrufen kann. Folgende Mechanismen sind möglich:

-   Machen Sie eine benutzerdefinierte COM-Schnittstelle verfügbar.
-   Automation-Eigenschaften werden über **IDispatch unterstützt.**
-   Machen Sie die **IPropertyBag-Schnittstelle** verfügbar, und definieren Sie einen Satz benannter Eigenschaften.

In diesem Beispiel wird eine benutzerdefinierte COM-Schnittstelle namens ISaturation verwendet. Dies ist keine tatsächliche DirectShow-Schnittstelle. sie wird nur für dieses Beispiel definiert. Deklarieren Sie zunächst die Schnittstelle in einer Headerdatei zusammen mit dem Schnittstellenbezeichner (IID):


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



Sie können die Schnittstelle auch mit IDL definieren und den MIDL-Compiler verwenden, um die Headerdatei zu erstellen. Implementieren Sie als Nächstes die benutzerdefinierte Schnittstelle im Filter. In diesem Beispiel werden die Methoden "Get" und "Set" für den Sättigungswert des Filters verwendet. Beachten Sie, dass beide Methoden den m \_ lSaturation-Member mit einem kritischen Abschnitt schützen.


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



Natürlich unterscheiden sich die Details Ihrer eigenen Implementierung von dem hier gezeigten Beispiel.

Weiter: [Schritt 2. Implementieren Sie ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> <dt>

[Erstellen einer Filtereigenschaftsseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



