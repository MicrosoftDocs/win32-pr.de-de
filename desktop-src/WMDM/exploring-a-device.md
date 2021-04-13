---
title: Untersuchen eines Geräts
description: Untersuchen eines Geräts
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Device Manager, untersuchen von Geräten
- Device Manager, untersuchen von Geräten
- Programmier Handbuch, untersuchen von Geräten
- Desktop Anwendungen, untersuchen von Geräten
- Erstellen von Windows Media Device Manager-Anwendungen, untersuchen von Geräten
- Untersuchen von Geräten
- Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388348"
---
# <a name="exploring-a-device"></a>Untersuchen eines Geräts

Das Durchsuchen eines Geräts ähnelt dem untersuchen eines Laufwerks. Alle Objekte auf einem Gerät werden als " *Speicher*" bezeichnet. Ein Speicher kann eine Datei, ein Ordner oder ein abstraktes Objekt (z. b. eine Wiedergabeliste) auf dem Gerät sein. Sie müssen die Attribute und Metadaten eines Speichers überprüfen (falls unterstützt), um zu verstehen, welche Art von Speicher er ist. Storages sind hierarchisch auf dem Gerät organisiert. jeder Speicher verfügt über genau ein übergeordnetes Element, und alle Speicher werden letztendlich von einem einzelnen Stamm Gerätespeicher mit dem Namen " \\ " abgeleitet.

In den folgenden Schritten wird beschrieben, wie Sie ein Gerät durchsuchen:

1.  Holen Sie sich die [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle eines Geräts, wie unter Auflisten von [Geräten](enumerating-devices.md)beschrieben.
2.  Rufen Sie [**iwmdmdevice:: enumstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) auf, um eine [**iwmdmenumstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) -Schnittstelle abzurufen. Diese Schnittstelle wird verwendet, um alle untergeordneten Objekte des Speichers zu erhalten, der diese Schnittstelle zurückgibt. Wenn Sie diese Schnittstelle vom Gerät erhalten, so wie es hier der Fall ist, enthält Sie nur einen Speicher: den Stamm Gerätespeicher.
3.  Rufen Sie [**iwmdmenumschlag:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) mit einer Anzahl von 1 auf, um die [**iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) -Schnittstelle für den Stamm Gerätespeicher abzurufen. (Sie können nicht mehr als ein untergeordnetes Element vom Gerät anfordern.)
4.  Überprüfen Sie alle Speicherplatz auf dem Gerät, indem Sie " [**iwmdmstorage:: enumstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) " rekursiv aufrufen und anschließend " **iwmdmenumstorage:: Next** ", um untergeordnete Elemente eines Speichers abzurufen. Wenn Sie feststellen möchten, ob ein Speicher über untergeordnete Elemente verfügt, um die Aufrufe von **enumstorage** und **Next** zu vermeiden, können Sie [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) aufrufen, um nach den Flags zu suchen, in denen WMDM \_ Storage \_ attr \_ Dateien aufweist, \_ oder der WMDM- \_ Speicher \_ attr \_ \_ Weitere Informationen zum Ermitteln der Eigenschaften eines Speichers finden Sie unter Get [and Setting Metadata and Attribute](getting-and-setting-metadata-and-attributes.md) und get [and Setting Metadata and Attribute in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).

Windows Media Device Manager macht keinen Standardsatz von Ordnern verfügbar, die Medien eines bestimmten Typs enthalten (z. b. den Ordner "meine Wiedergabe" für Wiedergabelisten). Jedes Gerät verfügt über ein eindeutiges Dateisystem, und Sie müssen sich an einem geeigneten Ort entscheiden, um eine bestimmte Datei zu suchen oder zu senden.

> [!Note]  
> In Windows-Explorer können virtuelle Ordner angezeigt werden, die nicht tatsächlich auf dem Gerät vorhanden sind. Virtuelle Beispiel Ordner sind die Ordner "Media" und "Data", die für MTP-Geräte angezeigt werden. Diese Ordner werden von Windows erstellt, um die Downloads für Endbenutzer zu vereinfachen. Sie sind nicht tatsächlich auf dem Gerät vorhanden. Die Anwendung sollte nicht von der Suche nach diesen Typen allgemeiner Ordner abhängen. Im Gegensatz dazu zeigt Windows-Explorer möglicherweise einige Ordner oder Objekte an, die auf dem Gerät vorhanden sind (z. b. Wiedergabelisten).

 

Der folgende C++-Beispielcode veranschaulicht die rekursive Untersuchung eines Geräts. Es verwendet zwei Funktionen:

-   "Exploredevice", eine Start Funktion, die einen Geräte Zeiger empfängt und einen Zeiger auf den Stamm Enumerator für dieses Gerät erhält.
-   Recursiveexplorestorage, das aufgerufen wird, um ein Gerät rekursiv zu untersuchen.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




