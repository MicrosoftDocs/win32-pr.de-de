---
description: In diesem Thema werden die Header und Bibliotheken aufgelistet, die alle Media Foundation-APIs definieren.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation-Header und-Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d5412f3f306c6e0d7327c1da1eb4c48bb109a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363020"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation-Header und-Bibliotheken

In diesem Thema werden die Header und Bibliotheken aufgelistet, die alle Media Foundation-APIs definieren.

Informationen zum Suchen des Headers und der Bibliothek für ein bestimmtes API-Element finden Sie auf den Referenzseiten in der [Media Foundation-Programmier Referenz](media-foundation-programming-reference.md).

## <a name="headers"></a>Header

-   codecapi. h
-   d3d11. h
-   d3d9. h
-   d3d9caps. h
-   d3d9types. h
-   DXVA. h
-   dxva2api. h
-   dxvahd. h
-   EVR. h
-   evr9. h
-   mfapi. h
-   "MF"-Engine. h
-   mferrors. h
-   mspdl. h
-   MF mediacapture. h
-   MF mediaengine. h
-   mfmp2dlna. h
-   mfobjects. h
-   MF. lib
-   "MF Play. h"
-   "mfreadwrite. h"
-   "MF Transform. h"
-   opmapi. h
-   wmcodecdsp. h
-   wmcontainer. h

## <a name="libraries"></a>Bibliotheken

-   dxva2. lib
-   EVR. lib
-   MF. lib
-   MF. lib
-   MF Play. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="library-changes-in-windows-7"></a>Bibliotheks Änderungen in Windows 7

Ab Windows 7 werden bestimmte Media Foundation Funktionen aus anderen DLL-Dateien exportiert als in früheren Versionen.

Diese Änderungen wirken sich auf die folgenden lib-Dateien aus:

-   EVR. lib
-   MF. lib
-   MF. lib

Eine Anwendung, die eine dieser Funktionen verwendet, muss abhängig von der SDK-Version und der Zielplattform mit einem anderen Satz von lib-Dateien verknüpft werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SDK-Version</th>
<th>Bibliotheken</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows SDK für Windows Vista<br/> Windows SDK für Windows Server 2008<br/></td>
<td>EVR. lib<br/> MF. lib<br/> MF. lib<br/></td>
</tr>
<tr class="even">
<td>Windows SDK für Windows 7</td>
<td>Wenn die Zielplattform Windows Vista oder Windows Server 2008 ist, verknüpfen Sie die folgenden Bibliotheken:<br/>
<ul>
<li>evr_vista. lib</li>
<li>mf_vista. lib</li>
<li>mfplat_vista. lib</li>
</ul>
Wenn die Zielplattform Windows 7 oder höher ist, verknüpfen Sie die folgenden Bibliotheken:<br/>
<ul>
<li>EVR. lib</li>
<li>MF. lib</li>
<li>MF. lib</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="additional-info-on-helper-functions"></a>Weitere Informationen zu Hilfsfunktionen

Der Windows 8-MFPlat.dll ist eine Komponente des Microsoft Windows-Betriebssystems. Es verfügt über mehrere Funktionen, die im Modul enthalten sind.

Mfplat implementiert Hilfsfunktionen für die Speicher Belegung auf niedriger Ebene, die Vorgangs Planung von FIFOs und die Win32-Datei Zugriffs Abstraktionen. Um spezifischere Informationen zu erhalten, bietet das Unterstützung für Folgendes:

-   zuordnen und Initialisieren von Speicher Puffern (als "Beispiele" bezeichnet) und Hilfe Hilfen zur Vereinfachung der Verwaltung Ihrer Lebensdauer
-   effiziente Funktionen zum Kopieren von Daten für Arbeitsspeicher Puffer
-   zuordnen und Initialisieren von Vorgangs-ffos (als "Ereignisse" bezeichnet)
-   Implementieren eines einfachen Clock-Objekts
-   Implementieren eines Win32-Datei-Wrappers
-   zuordnen und Initialisieren von Arrays von Speicher Puffern für CPUs und GPUs

Wenn die [**MF Startup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Methode erfolgreich ist, stellt MF die folgenden Funktionen der Arbeits Warteschlange bereit:

-   intern unterstützende e/a-Elemente (wie von Win32-Datei Wrapper und socketbibliotheken verwendet)
-   Bereitstellen eines Arrays von multithreadarbeitswarteschlangen mit Unterstützung für Thread Priorität
-   unterstützen von Arbeits Elementen, Zeit Geber Elementen und warte Elementen über die Arbeits Warteschlangen

Mfplat bietet Hilfsfunktionen zum Suchen und Erstellen von Medien Transformationen und Medienquellen, die im System registriert sind, sowie zum Erstellen und Bearbeiten von Medientypen, obwohl mfplat selbst das eigentliche Medium nicht erstellen oder wiedergeben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




