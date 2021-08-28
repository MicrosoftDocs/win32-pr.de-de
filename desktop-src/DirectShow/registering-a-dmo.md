---
description: Registrieren eines DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrieren eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5635f7b05edb13da80adb62104db5c412fa55608ec2f9b5214380b7d9a095e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904540"
---
# <a name="registering-a-dmo"></a>Registrieren eines DMO

Damit Clients Ihre DMO verwenden können, muss die CLSID auf dem System des Benutzers registriert werden. Dies erfolgt über die **DllRegisterServer-Funktion der** DLL. Wenn Sie die At Active Template Library (ATL) verwenden, generiert der ATL-Assistent diese Funktion automatisch.

Sie können Ihre Daten auch DMO einer oder mehrere Standardkategorien DMO registrieren. Dadurch können Clients Ihre DMO mithilfe der [**DMOEnum-Funktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) finden. Die Kategorien werden durch GUID definiert und im Abschnitt mit den [GUIDs DMO aufgeführt.](dmo-guids.md)

Das Registrieren DMO unter einer Kategorie ist optional. Rufen Sie dazu die [**DMORegister-Funktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) auf, und geben Sie den DMO, die CLSID und die Kategorie an. Optional können Sie auch eine Reihe von Medientypen registrieren, die von Ihren DMOs unterstützt werden. Weitere Informationen finden Sie unter [DMO Medientypen.](dmo-media-types.md)

Das folgende Beispiel zeigt, wie Sie einen Audioeffekt für DMO registrieren, der PCM-Audioeingabe und -ausgabe unterstützt. In diesem Fall sind die Eingabe- und Ausgabetypen identisch.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



In diesem Beispiel wird davon ausgegangen, dass ATL zum Erstellen des Projekts verwendet wurde. Die letzte Zeile der Funktion ruft die ATL-Standardmethode auf, um den COM-Server zu registrieren. Wenn Sie ATL nicht verwenden, sieht Ihre Funktion anders aus.

**Aufheben der Registrierung eines DMO**

Ihre **DllUnregisterServer-Funktion** muss alle Registrierungseinträge entfernen, die von der **DllRegisterServer-Funktion** erstellt werden. Wenn Sie beim Registrieren des DMO **DMORegister** aufrufen, müssen Sie [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) mit der gleichen Kategorie registrieren, wenn Sie die Registrierung der DMO.

Im folgenden Beispiel werden die im vorherigen Beispiel erstellten Registrierungseinträge entfernt:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow-Werte**

Zum Erstellen von Filterdiagrammen weist DirectShow DMOs einen Standardwert zu. Sie können diesen Wert überschreiben, indem Sie dem Registrierungsschlüssel des DMO in HKEY \_ CLASSES \_ ROOT CLSID einen \\ Registrierungseintrag hinzufügen. Schließen Sie einen **DWORD-Wert** mit dem Namen `Merit` ein, dessen Wert den Zierwert angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



