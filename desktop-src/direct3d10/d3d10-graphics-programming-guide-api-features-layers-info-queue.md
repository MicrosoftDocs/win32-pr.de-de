---
description: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753830"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)

Die Informationswarteschlange wird von einer Schnittstelle verwaltet (siehe [**ID3D10InfoQueue-Schnittstelle),**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)die Debugmeldungen speichert, abruft und filtert. Die Warteschlange besteht aus: einer Nachrichtenwarteschlange, einem optionalen Speicherfilterstapel und einem optionalen Abruffilterstapel. Der Speicherfilterstapel kann verwendet werden, um die Nachrichten zu filtern, die Sie speichern möchten. der Abruf-Filter-Stapel kann verwendet werden, um die Nachrichten zu filtern, die Sie speichern möchten. Nachdem Sie eine Nachricht gefiltert haben, wird die Nachricht im Debugfenster ausgegeben und im entsprechenden Stapel gespeichert.

Im Allgemeinen:

-   Rufen Sie [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) auf, um benutzerdefinierte Nachrichten zu generieren.
-   Der Aufruf [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) wird verwendet, um Nachrichten abzurufen (die einen optionalen Abruffilter übergeben).

## <a name="registry-controls"></a>Registrierungssteuerelemente

Verwenden Sie Registrierungsschlüssel, um Filtereinstellungen anzupassen, Haltepunkte anzupassen und die Debugausgabe zu stummschalten. Die Debugebene überprüft diese Pfade auf Registrierungsschlüssel. Der erste gefundene Pfad wird verwendet.

1.  HKCU \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierten Unterschlüssel>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierten Unterschlüssel>
3.  HKCU \\ Software \\ Microsoft \\ Direct3D

Hierbei gilt:

-   HKCU steht für HKEY \_ CURRENT \_ USER und HKLM für HKEY \_ LOCAL \_ MACHINE.
-   <benutzerdefinierten Unterschlüssel> ist ein beliebiger Name zum Speichern von Debugeinstellungen für eine Anwendung.

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtern von Debugmeldungen mit registrierungsschlüsseln

Wenn die Registrierung einen InfoQueueStorageFilterOverride-Schlüssel enthält (und ungleich null ist), können Nachrichten (und Debugausgaben) gefiltert werden, indem die folgenden Registrierungssteuerelemente hinzugefügt werden.

-   DWORD Mute \_ CATEGORY \_ \* : Debugausgabe, wenn dieser Schlüssel ungleich 0 (null) ist.
-   DWORD Mute \_ SEVERITY \_ \* : Die Debugausgabe ist deaktiviert, wenn dieser Schlüssel ungleich 0 (null) ist.
-   DWORD-Mute-ID: \_ \_ \* Nachrichtenname oder -nummer kann für verwendet werden \* (genau wie bei der \_ zuvor beschriebenen BreakOn-ID). \_ \* Die Debugausgabe ist deaktiviert, wenn dieser Schlüssel ungleich 0 (null) ist.
-   DWORD Unmute SEVERITY INFO : \_ \_ Die Debugausgabe ist AKTIVIERT, wenn dieser Schlüssel ungleich 0 (null) ist. Wenn InfoQueueStorageFilterOverride aktiviert ist, werden Debugmeldungen mit dem Schweregrad INFO standardmäßig stummgeschaltet. Daher kann INFO für diesen Schlüssel wieder aktiviert werden.

Diese Steuerelemente ändern, ob eine Nachricht aufgezeichnet oder angezeigt wird. sie wirken sich nicht darauf aus, ob eine API erfolgreich ist oder fehlschlägt.

### <a name="setting-break-conditions-using-registry-keys"></a>Festlegen von Unterbrechungsbedingungen mithilfe von Registrierungsschlüsseln

Anwendungen können mithilfe der folgenden Registrierungsschlüssel gezwungen werden, eine Nachricht zu unterbrechen.

**EnableBreakOnMessage:** Dieser Schlüssel ermöglicht das Abbrechen von Nachrichten (und bewirkt, dass die Einstellungen von SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() ignoriert werden. Die tatsächlichen Nachrichten, für die ein Breakbreak ausgeführt werden soll, werden mit einem oder mehreren \_ \* unten definierten BreakOn-Werten definiert.

-   **BreakOn \_ \_CATEGORY \** _ – Unterbrechung bei jeder Nachricht, die die Speicherfilter durchläuft. \_ ist eine der D3D10 \_ MESSAGE \_ CATEGORY-Meldungen.
-   **BreakOn \_ SEVERITY \_ \** _ – Unterbrechung bei jeder Nachricht, die die Speicherfilter durchläuft. \_ ist eine der D3D10 \_ MESSAGE \_ \_ SEVERITY-Meldungen.
-   **BreakOn \_ \_ID \** _ – Unterbrechung bei jeder Nachricht, die die Speicherfilter durchläuft. \_ ist eine der D3D10 \_ MESSAGE \_ \_ ID-Meldungen oder kann der numerische Wert der Fehlerenumeration sein. Angenommen, die Nachricht mit der ID "D3D10 \_ MESSAGE \_ ID \_ HYPOTHETISCH" hat den Wert 123 in der D3D10 \_ MESSAGE \_ ID-Enumeration. In diesem Fall würde das Erstellen des Werts BreakOn \_ ID \_ HYPOTHETISCH=1 oder \_ BreakOn-ID \_ 123=1 das gleiche erreichen: break, wenn eine Nachricht mit der ID D3D10 \_ MESSAGE ID \_ \_ HYPOTHETISCH gefunden wird.

### <a name="muting-debug-output-using-registry-keys"></a>Stummschalten der Debugausgabe mit registrierungsschlüsseln

Die Debugausgabe kann mithilfe eines MuteDebugOutput-Schlüssels stummgeschaltet werden. Das Vorhandensein dieses Werts in der Registrierung erzwingt die Außerkraftsetzung der [**ID3D10InfoQueue::SetMuteDebugOutput-Methode**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) von InfoQueue. MuteDebugOutput verhindert, dass Nachrichten, die den Speicherfilter übergeben, an die Debugausgabe gesendet werden.

## <a name="disabling-debug-layer-messages"></a>Deaktivieren von Meldungen der Debugebene

Debugebenenmeldungen können einzeln oder als Gruppe zur Laufzeit deaktiviert werden, indem Filter mit [**id3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries)angegeben werden. Das *pFilter-Argument* für **ID3D10InfoQueue::AddStorageFilterEntries** nimmt eine [**D3D10 \_ INFO QUEUE \_ \_ FILTER-Struktur**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) an, die eine Liste der Zulässigen und eine Verweigerungsliste enthält. Die Listen "Zulassen" und "Verweigern" werden von [**D3D10 \_ INFO QUEUE FILTER \_ \_ \_ DESC-Strukturen**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) beschrieben, die es ermöglichen, filtering nach "catergory", "severity" und "individual message ID" anzugeben.

Der folgende Code ist ein Beispiel für das Einrichten der [**ID3D10InfoQueue-Schnittstelle,**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) um die Nachricht D3D10 \_ MESSAGE ID DEVICE DRAW INDEX BUFFER TOO SMALL zu \_ \_ \_ \_ \_ \_ \_ verweigern.


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

 

 



