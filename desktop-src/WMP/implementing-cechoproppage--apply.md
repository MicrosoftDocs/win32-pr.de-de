---
title: Implementieren von CEchoPropPage Apply
description: Implementieren von CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispiel-Eigenschaftenseiten
- Plug-Ins, Echo-Beispieleigenschaftsseiten
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel-Eigenschaftenseiten
- DSP-Plug-Ins, Echo-Beispiel-Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel, Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel, CEchoPropPage Apply-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a53d05bee90908f766034c300c99bcfa8d529b06e6713c803bd99bcf042b579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135623"
---
# <a name="implementing-cechoproppageapply"></a>Implementieren von CEchoPropPage::Apply

Die CEchoPropPage::Apply-Methode wird in EchoPropPage.cpp implementiert. Er wird ausgeführt, wenn  der Benutzer im Eigenschaftenseitendialogfeld in der Windows Media Player. Der Beispielcode des Plug-In-Assistenten stellt eine Implementierung für die Handhabung einer einzelnen Eigenschaft zur Auswahl. Sie können diesen Code für eine der Echo-Beispieleigenschaften ändern und dann Code hinzufügen, um den anderen Eigenschaftswert zu speichern.

## <a name="declaring-the-apply-method-variables"></a>Deklarieren der Apply-Methodenvariablen

Zunächst müssen Sie die Deklaration von fScaleFactor entfernen. Fügen Sie dann variablen Deklarationen hinzu, die Sie benötigen. Das folgende Beispiel zeigt die abgeschlossenen Variablendeklarationen:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Abrufen der Werte von der Eigenschaftenseite

Sie müssen Code implementieren, um die Benutzereingabe abzurufen und zu überprüfen. Im folgenden Codebeispiel wird der Wert für die Verzögerungszeit aus dem Bearbeitungsfeld IDC DELAYTIME abgerufen und dann überprüft, ob sich der Wert innerhalb eines \_ angegebenen Bereichs befindet:


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



Wenn sich die Benutzereingabe nicht im angegebenen Bereich befindet, zeigt der Code ein Meldungsfeld an. Beachten Sie die Verwendung der Zeichenfolgenressource, die Sie zuvor für die Fehlermeldung erstellt haben.

Im folgenden Beispiel wird die Effektebene aus dem Bearbeitungsfeld IDC VERDRMIX abgerufen und dann überprüft, ob sich der Wert innerhalb eines \_ angegebenen Bereichs befindet:


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>Speichern der Eigenschaftswerte in der Registrierung

Als Nächstes muss Ihr Code die neuen Eigenschaftswerte in der Registrierung beibehalten. Im folgenden Code werden beide Eigenschaftswerte gespeichert:


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>Aktualisieren der Echo Plug-In-Eigenschaftswerte

Die **Apply-Methode** muss das Echo-Plug-In darüber informieren, dass sich die Eigenschaftswerte geändert haben. Der folgende Code ruft die put-Eigenschaftsmethode für jede Eigenschaft mithilfe des Schnittstellenzeigers auf, der in CEchoPropPage::SetObjects abgerufen wurde:


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



Beachten Sie, dass der Vermischungswert in einen Gleitkomma konvertiert wird, bevor er an das Plug-In übergeben wird.

## <a name="disabling-the-apply-button"></a>Deaktivieren der Schaltfläche "Anwenden"

Im letzten Schritt sollte der Code Anwenden im Dialogfeld der Eigenschaftenseite deaktivieren, um dem Benutzer zu signalisieren, dass die Werte erfolgreich aktualisiert wurden. Dies erfordert die folgende einzelne Codezeile:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaftenseite des Echobeispiels**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




