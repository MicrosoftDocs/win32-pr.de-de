---
description: Aufzählen von Effekten und Übergängen
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Aufzählen von Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345397"
---
# <a name="enumerating-effects-and-transitions"></a>Aufzählen von Effekten und Übergängen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

DirectShow stellt ein [System Geräte-Enumeratorobjekt](system-device-enumerator.md) zum Auflisten von Geräten bereit. Sie können Sie verwenden, um Moniker für Effekte oder Übergänge abzurufen, die auf dem System des Benutzers installiert sind.

Der Enumerator für Systemgeräte macht die [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle verfügbar. Es werden kategorieenumeratoren für angegebene Gerätekategorien zurückgegeben. Ein kategorieenumerator wiederum macht die [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) -Schnittstelle verfügbar und gibt Moniker für jedes Gerät in der Kategorie zurück. Eine ausführliche Erläuterung der Verwendung von **ikreatedevenum** finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md). Im folgenden finden Sie eine kurze Zusammenfassung, die speziell für DirectShow-Bearbeitungs Dienste gilt.

Führen Sie die folgenden Schritte aus, um Effekte oder Übergänge aufzuzählen.

1.  Erstellen Sie eine Instanz des Enumerators für Systemgeräte.
2.  Rufen Sie die [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) -Methode auf, um einen kategorieenumerator abzurufen. Kategorien werden durch Klassen Bezeichner (CLSIDs) definiert. Verwenden Sie CLSID- \_ VideoEffects1Category für Effekte oder CLSID \_ VideoEffects2Category für Übergänge.
3.  Rufen Sie **IEnumMoniker:: Next** auf, um jeden Moniker in der-Enumeration abzurufen.
4.  Rufen Sie für jeden Moniker **IMoniker:: bindesstorage** auf, um den zugehörigen Eigenschaften Behälter abzurufen.

Der Eigenschaften Behälter enthält den anzeigen Amen und die Globally Unique Identifier (GUID) für den Effekt oder den Übergang. Eine Anwendung kann eine Liste von anzeigen Amen anzeigen und dann die entsprechende GUID abrufen.

Diese Schritte werden im folgenden Codebeispiel veranschaulicht.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
