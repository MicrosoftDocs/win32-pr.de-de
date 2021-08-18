---
title: Implementieren von CEcho FinalConstruct
description: Implementieren von CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispieleigenschaftsseiten
- Plug-Ins, Echo-Beispieleigenschaftsseiten
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel-Eigenschaftenseiten
- DSP-Plug-Ins, Echo-Beispiel-Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel, Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel, CEcho FinalConstruct-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748145"
---
# <a name="implementing-cechofinalconstruct"></a>Implementieren von CEcho::FinalConstruct

Die CEcho::FinalConstruct-Methode wird in Echo.cpp implementiert. Sie enthält Code zum Lesen der Eigenschaftswerte aus der Registrierung, wenn Windows Media Player DSP-Plug-In-Objekt instanziiert. Dies ist wichtig, da die Benutzereinstellungen zwischen Instanzen des Objekts sowie zwischen Sitzungen beibehalten werden können. Der Beispielcode des Plug-In-Assistenten bietet implementierungsbasierte Informationen zum Lesen einer einzelnen Eigenschaft aus der Registrierung. Sie können diesen Code ändern, um die Delay Time-Eigenschaft zu behandeln, und dann Code hinzufügen, um den Vermischungsmischungs-Eigenschaftswert zu lesen.

Der folgende Beispielcode liest jeden Eigenschaftswert aus der Registrierung und speichert jeden in der richtigen Membervariablen:


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



Beachten Sie, dass der DWORD-Wert für die Vermischung in einen Gleitkommawert konvertiert wird. Beachten Sie auch, dass der Code den richtigen Wert für m \_ fDryMix berechnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaftenseite des Echobeispiels**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




