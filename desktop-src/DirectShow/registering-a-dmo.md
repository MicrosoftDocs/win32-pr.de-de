---
description: Registrieren eines DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrieren eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346593"
---
# <a name="registering-a-dmo"></a>Registrieren eines DMO

Damit Clients ihren DMO verwenden können, muss die CLSID auf dem System des Benutzers registriert werden. Dies erfolgt über die **DllRegisterServer** -Funktion der dll. Wenn Sie die Active Template Library (ATL) verwenden, wird diese Funktion vom ATL-Assistenten automatisch generiert.

Sie können Ihre DMO auch unter mindestens einer DMO-Standard Kategorie registrieren. Dadurch können Clients ihre DMO mithilfe der [**dmoenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion ermitteln. Die Kategorien werden durch die GUID definiert und sind im Abschnitt [DMO GUIDs](dmo-guids.md)aufgeführt.

Das Registrieren eines DMO unter einer Kategorie ist optional. Dazu müssen Sie die [**dmoregiester**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) -Funktion und den anzeigen amen des DMO, der CLSID und der Kategorie angeben. Optional können Sie auch einen Satz von Medientypen registrieren, die von ihren DMOS unterstützt werden. Weitere Informationen finden Sie unter [DMO Media Types](dmo-media-types.md).

Im folgenden Beispiel wird gezeigt, wie Sie einen Audioeffekt-DMO registrieren, der PCM-Audioeingabe und-Ausgabe unterstützt. In diesem Fall sind die Eingabe-und Ausgabetypen identisch.


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



In diesem Beispiel wird davon ausgegangen, dass ATL zum Erstellen des Projekts verwendet wurde. die letzte Zeile der-Funktion Ruft die Standard-ATL-Methode auf, um den com-Server zu registrieren. Wenn Sie ATL nicht verwenden, sieht die Funktion anders aus.

**Aufheben der Registrierung eines DMO**

Die **DllUnregisterServer** -Funktion muss alle Registrierungseinträge entfernen, die von der **DllRegisterServer** -Funktion erstellt werden. Wenn Sie **dmoregister** beim Registrieren des DMO aufzurufen, müssen Sie [**dmounregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) bei der Registrierung des DMO bei der Aufhebung der Registrierung in derselben Kategorie durch dmounregistrieren.

Im folgenden Beispiel werden die im vorherigen Beispiel erstellten Registrierungseinträge entfernt:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow-Verdienst Werte**

Zum Zweck der Erstellung von Filter Diagrammen weist DirectShow DMOS einen Standardwert für den Verdienst zu. Sie können diesen Wert überschreiben, indem Sie einen Registrierungs Eintrag zum Registrierungsschlüssel von DMO in HKEY \_ Classes \_ root \\ CLSID hinzufügen. Fügen Sie einen **DWORD** -Wert mit dem Namen ein, `Merit` dessen Wert den Verdienst angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



