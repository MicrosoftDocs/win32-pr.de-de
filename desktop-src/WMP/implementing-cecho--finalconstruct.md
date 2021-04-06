---
title: Implementieren von Cecho FinalConstruct
description: Implementieren von Cecho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Cecho FinalConstruct-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100690"
---
# <a name="implementing-cechofinalconstruct"></a>Implementieren von Cecho:: FinalConstruct

Die Cecho:: FinalConstruct-Methode ist in Echo. cpp implementiert. Es enthält Code zum Lesen der Eigenschaftswerte aus der Registrierung, wenn Windows Media Player das DSP-Plug-in-Objekt instanziiert. Dies ist wichtig, da die Benutzereinstellungen zwischen Instanzen des Objekts und zwischen Sitzungen beibehalten werden können. Der Beispielcode des Plug-in-Assistenten bietet eine Implementierung zum Lesen einer einzelnen Eigenschaft aus der Registrierung. Sie können diesen Code ändern, um die Eigenschaft Verzögerungszeit zu verarbeiten, und dann Code hinzufügen, um den Eigenschafts Wert für die nasse Mischung zu lesen.

Im folgenden Beispielcode wird jeder Eigenschafts Wert aus der Registrierung gelesen und in der richtigen Element Variablen gespeichert:


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



Beachten Sie, dass der DWORD-Wert für die nasse Mischung in einen Gleit Komma Wert konvertiert wird. Beachten Sie auch, dass der Code den korrekten Wert für m-"sssmix" berechnet \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




