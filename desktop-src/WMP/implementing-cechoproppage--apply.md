---
title: Implementieren von cechoproppage Apply
description: Implementieren von cechoproppage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, cechoproppage Apply-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856315"
---
# <a name="implementing-cechoproppageapply"></a>Implementieren von cechoproppage:: apply

Die cechoproppage:: Apply-Methode ist in "echoproppage. cpp" implementiert. Sie wird ausgeführt, wenn der Benutzer im Dialogfeld Eigenschaften Seite in Windows **Media Player auf übernehmen klickt.** Der Beispielcode des Plug-in-Assistenten stellt eine-Implementierung bereit, um eine einzelne Eigenschaft zu verarbeiten. Sie können diesen Code für eine der Echo-Beispiel Eigenschaften ändern und dann Code hinzufügen, um den anderen Eigenschafts Wert zu speichern.

## <a name="declaring-the-apply-method-variables"></a>Deklarieren der Variablen der Apply-Methode

Zuerst müssen Sie die Deklaration von "f" entfernen. Fügen Sie dann die Variablen Deklarationen hinzu, die Sie benötigen. Das folgende Beispiel zeigt die abgeschlossenen Variablen Deklarationen:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Abrufen der Werte von der Eigenschaften Seite

Sie müssen Code implementieren, um die Benutzereingabe abzurufen und zu überprüfen. Im folgenden Codebeispiel wird der Wert für die Verzögerungszeit aus dem IDC \_ -Delta-Bearbeitungsfeld abgerufen und dann überprüft, ob der Wert innerhalb eines angegebenen Bereichs liegt:


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



Wenn sich die Benutzereingabe nicht im angegebenen Bereich befindet, zeigt der Code ein Meldungs Feld an. Beachten Sie die Verwendung der Zeichen folgen Ressource, die Sie zuvor für die Fehlermeldung erstellt haben.

Im folgenden Beispiel wird die Effekt Ebene aus dem Feld "IDC \_ wetmix" abgerufen und dann überprüft, ob der Wert innerhalb eines angegebenen Bereichs liegt:


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

Als nächstes muss der Code die neuen Eigenschaftswerte in der Registrierung speichern. Der folgende Code speichert beide Eigenschaftswerte:


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



## <a name="updating-the-echo-plug-in-property-values"></a>Aktualisieren der Eigenschaftswerte des Echo-Plug-ins

Die **Apply** -Methode muss das Echo-Plug-in darüber informieren, dass sich die Eigenschaftswerte geändert haben. Der folgende Code Ruft die-Eigenschaft Put-Methode für jede Eigenschaft mit dem Schnittstellen Zeiger auf, der in cechoproppage:: SetObjects abgerufen wurde:


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



Beachten Sie, dass der Wert der nass Mischung in den Gleit Komma Wert konvertiert wird, bevor er an das Plug-in übermittelt wird.

## <a name="disabling-the-apply-button"></a>Deaktivieren der Schaltfläche "anwenden"

Im letzten Schritt sollte der Code die Apply-Eigenschaft im Dialogfeld Eigenschaften Seite als Signal an den Benutzer deaktivieren, dass die Werte erfolgreich aktualisiert wurden. Hierfür ist die folgende einzelne Codezeile erforderlich:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




