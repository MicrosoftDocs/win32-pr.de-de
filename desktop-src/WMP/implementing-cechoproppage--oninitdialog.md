---
title: Implementieren von cechoproppage OnInitDialog
description: Implementieren von cechoproppage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, cechoproppage OnInitDialog-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342042"
---
# <a name="implementing-cechoproppageoninitdialog"></a>Implementieren von cechoproppage:: OnInitDialog

Die **cechoproppage:: OnInitDialog** -Methode ist in "echoproppage. cpp" implementiert. Sie wird ausgeführt, wenn das Dialogfeld Eigenschaften Seite aufgerufen wird. Der Code in dieser Methode muss die aktuellen Eigenschaftswerte abrufen und im richtigen Bearbeitungsfeld anzeigen. Der Beispielcode des Plug-in-Assistenten stellt eine Implementierung für eine einzelne Eigenschaft bereit. Sie können diesen Code für eine der Echo-Beispiel Eigenschaften ändern und dann Code hinzufügen, um den zweiten Eigenschafts Wert abzurufen.

## <a name="declaring-the-oninitdialog-method-variables"></a>Deklarieren der OnInitDialog-Methoden Variablen

Zunächst müssen Sie die Deklaration von "f" entfernen und durch die folgenden Variablen Deklarationen ersetzen:


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Abrufen der aktuellen Werte aus dem Plug-in

Der Code sollte als nächstes versuchen, die aktuellen Eigenschaftswerte aus dem Echo-Plug-in abzurufen. Im folgenden Beispiel wird versucht, jede Eigenschaft abzurufen:


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



Im Dialogfeld wird der Wert für die Effekte-Ebene als ganze Zahl angezeigt, aber das Plug-in speichert den Wert als Gleit Komma Zahl. Daher konvertiert der Code den Gleit Komma Wert in einen **DWORD** -Wert.

## <a name="retrieving-the-current-values-from-the-registry"></a>Abrufen der aktuellen Werte aus der Registrierung

Wenn die Eigenschaften Seite die aktuellen Werte aus dem Plug-in nicht abrufen kann, muss Sie versuchen, Sie aus der Registrierung zu lesen. Der folgende Code liest die einzelnen Eigenschaftswerte:


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



Beachten Sie die Verwendung der zuvor erstellten Registrierungs Konstanten.

## <a name="displaying-the-values-to-the-user"></a>Anzeigen der Werte für den Benutzer

Zum Schluss muss auf der Eigenschaften Seite die Werte in den richtigen Bearbeitungsfeld-Steuerelementen angezeigt werden. Der folgende Beispielcode veranschaulicht dies:


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




