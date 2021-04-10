---
description: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041466"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)

Die Informations Warteschlange wird von einer Schnittstelle (siehe [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) verwaltet, die Debugmeldungen speichert, abruft und filtert. Die Warteschlange besteht aus: einer Nachrichten Warteschlange, einem optionalen Speicher Filter Stapel und einem optionalen Abruf Filter Stapel. Der Speicher Filter Stapel kann verwendet werden, um die Nachrichten zu filtern, die gespeichert werden sollen. der Abruf Filter Stapel kann verwendet werden, um die Nachrichten zu filtern, die gespeichert werden sollen. Nachdem Sie eine Meldung gefiltert haben, wird die Nachricht im Debugfenster ausgegeben und im entsprechenden Stapel gespeichert.

Im Allgemeinen:

-   Rufen Sie [**ID3D10InfoQueue:: addapplicationmessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) auf, um benutzerdefinierte Meldungen zu generieren.
-   Aufrufen von [**ID3D10InfoQueue:: getMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) dient zum Abrufen von Nachrichten (die einen optionalen Abruf Filter übergeben).

## <a name="registry-controls"></a>Registrierungs Steuerelemente

Verwenden Sie die Registrierungsschlüssel zum Anpassen von Filtereinstellungen, zum Anpassen von Breakpoints und zum stumm schalten der Debugausgabe. Die debugschicht prüft diese Pfade auf Registrierungsschlüssel. der erste gefundene Pfad wird verwendet.

1.  HKCU \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierter Unterschlüssel>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierter Unterschlüssel>
3.  HKCU- \\ Software \\ Microsoft \\ Direct3D

Hierbei gilt:

-   HKCU steht für HKEY \_ Current \_ User und HKLM für HKEY \_ local \_ Machine.
-   <benutzerdefinierter Unterschlüssel> ein beliebiger Name zum Speichern der Debugeinstellungen für eine Anwendung ist.

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtern von Debugmeldungen mithilfe von Registrierungs Schlüsseln

Wenn die Registrierung einen infoqueuestoragefilteroverride-Schlüssel enthält (und nicht NULL ist), können Nachrichten (und Debugausgaben) gefiltert werden, indem Sie die folgenden Registrierungs Steuerelemente hinzufügen.

-   DWORD stumm \_ Kategorie \_ \* -Debugausgabe, wenn dieser Schlüssel ungleich 0 (null) ist.
-   DWORD-Wert zum stumm schalten \_ \_ \* : die Debug-Ausgabe ist deaktiviert, wenn dieser Schlüssel nicht NULL ist.
-   DWORD \_ -stumm \_ \* -ID: der Name oder die Nummer der Nachricht kann für verwendet werden \* (genau wie bei der zuvor beschriebenen breakon- \_ ID \_ \* ). Die Debugausgabe ist deaktiviert, wenn dieser Schlüssel ungleich 0 (null) ist.
-   DWORD: unstumm \_ Schweregrad \_ Info-die Debug-Ausgabe ist aktiviert, wenn dieser Schlüssel nicht 0 (null) ist. Wenn infoqueuestoragefilteroverride aktiviert ist, werden standardmäßig Debugmeldungen mit dem Schweregrad Info stumm geschaltet. Daher können für diesen Schlüssel die Informationen wieder aktiviert werden.

Diese Steuerelemente ändern, ob eine Nachricht aufgezeichnet oder angezeigt wird. Sie haben keine Auswirkung darauf, ob eine API erfolgreich verläuft oder fehlschlägt.

### <a name="setting-break-conditions-using-registry-keys"></a>Festlegen von Abbruch Bedingungen mithilfe von Registrierungs Schlüsseln

Anwendungen können mit den folgenden Registrierungs Schlüsseln gezwungen werden, eine Nachricht zu unterbrechen.

**Enableatemkonmessage** : dieser Schlüssel ermöglicht das Unterbrechen von Nachrichten (und bewirkt, dass die Einstellungen für "setbreakoncategory ()/SetBreakOnSeverity ()/SetBreakOnID ()" ignoriert werden). Die eigentlichen Nachrichten, für die die Unterbrechung durchlaufen werden soll, werden mit einem oder mehreren Break on- \_ \* Werten definiert

-   **Break on \_ \_Kategorie \** _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft. \_ ist eine der \_ \_ kategorienachrichten der d3d10-Nachricht.
-   **Break on \_ Schwere \_ \* Grad* _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft. \_ ist eine der \_ Nachrichten Schweregrade der d3d10-Nachricht \_ \_ .
-   **Break on \_ \_ID \** _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft. \_ ist eine der d3d10- \_ \_ Nachrichten-ID- \_ Nachrichten oder kann der numerische Wert der Error-Enumeration sein. Nehmen wir beispielsweise an, dass die Nachricht mit der ID "d3d10 \_ Message \_ ID \_ hypothetisch" den Wert 123 in der d3d10-nach \_ richten-ID- \_ Enumeration enthielt. In diesem Fall würde das Erstellen der Wert breakon- \_ ID \_ hypothetisch = 1 oder breakon \_ ID \_ 123 = 1 denselben Vorgang unterbrechen, wenn eine Nachricht mit der ID d3d10 \_ Message \_ ID \_ hypothetisch vorkommt.

### <a name="muting-debug-output-using-registry-keys"></a>Muting Debugausgabe mithilfe von Registrierungs Schlüsseln

Die Debugausgabe kann mit einem mutedebugoutput-Schlüssel stumm geschaltet werden. Das vorhanden sein dieses Werts in der Registrierung erzwingt das Überschreiben der [**ID3D10InfoQueue:: setmutedebugoutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) -Methode der infoqueue. "Mutedebugoutput" beendet Nachrichten, die den Speicher Filter übergeben, an die Debugausgabe.

## <a name="disabling-debug-layer-messages"></a>Debugebenennachrichten werden deaktiviert.

Debugebenennachrichten können einzeln oder als Gruppe zur Laufzeit deaktiviert werden, indem Filter mithilfe von [**ID3D10InfoQueue:: addstoragefilterentries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries)angegeben werden. Das *pFilter* -Argument für **ID3D10InfoQueue:: addstoragefilterentries** übernimmt eine [**d3d10 \_ Info Queue- \_ \_ Filter**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) Struktur, die eine Zulassungsliste und eine Verweigerungs Liste enthält. Die Zulassungs-und Verweigerungs Listen werden von den [**d3d10 \_ Info \_ Queue \_ Filter \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) -Strukturen beschrieben, die die Angabe von Filtern durch catergory, Schweregrad und einzelne Nachrichten-ID ermöglichen.

Der folgende Code ist ein Beispiel für das Einrichten der [**ID3D10InfoQueue-Schnittstelle**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) zum Verweigern der d3d10-nach \_ richten- \_ ID \_ Geräte \_ \_ Index \_ Puffer \_ zu \_ klein.


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Ebenen](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



