---
description: 'Schritt 1:'
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 'Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368034"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft

Der Filter muss eine Methode unterstützen, mit der die Eigenschaften Seite damit kommunizieren kann, damit die Eigenschaften Seite Eigenschaften des Filters festlegen und abrufen kann. Folgende Mechanismen sind möglich:

-   Macht eine benutzerdefinierte COM-Schnittstelle verfügbar.
-   Unterstützung von Automatisierungs Eigenschaften über **IDispatch**.
-   Macht die **IPropertyBag** -Schnittstelle verfügbar und definiert einen Satz benannter Eigenschaften.

In diesem Beispiel wird eine benutzerdefinierte COM-Schnittstelle mit dem Namen isaturierung verwendet. Dabei handelt es sich nicht um eine tatsächliche DirectShow-Schnittstelle. Er ist nur für dieses Beispiel definiert. Beginnen Sie, indem Sie die-Schnittstelle in einer Header Datei zusammen mit dem Schnittstellen Bezeichner (IID) deklarieren:


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



Sie können auch die Schnittstelle mit IDL definieren und den Mittelpunkt Compiler zum Erstellen der Header Datei verwenden. Implementieren Sie anschließend die benutzerdefinierte Schnittstelle im Filter. In diesem Beispiel werden die Methoden "Get" und "Set" für den Sättigungswert des Filters verwendet. Beachten Sie, dass beide Methoden den m \_ lsättigung-Member mit einem kritischen Abschnitt schützen.


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



Die Details Ihrer eigenen Implementierung unterscheiden sich natürlich von dem hier gezeigten Beispiel.

Weiter: [Schritt 2. Implementieren Sie ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



