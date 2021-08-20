---
description: In diesem Thema werden die Header und Bibliotheken aufgeführt, die alle Media Foundation-APIs definieren.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation Header und Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6db7650c98f6491fa6db4010273475b4bd103a2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467467"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation Header und Bibliotheken

In diesem Thema werden die Header und Bibliotheken aufgeführt, die alle Media Foundation-APIs definieren.

Informationen zum Suchen des Headers und der Bibliothek für ein bestimmtes API-Element finden Sie auf den Referenzseiten in der Media Foundation [Programmierreferenz.](media-foundation-programming-reference.md)

## <a name="headers"></a>Header

-   codecapi.h
-   d3d11.h
-   d3d9.h
-   d3d9caps.h
-   d3d9types.h
-   dxva.h
-   dxva2api.h
-   dxvahd.h
-   evr.h
-   evr9.h
-   mfapi.h
-   mfcaptureengine.h
-   mferrors.h
-   mfidl.h
-   mfmediacapture.h
-   mfmediaengine.h
-   mfmp2dlna.h
-   mfobjects.h
-   mfplat.lib
-   mfplay.h
-   mfreadwrite.h
-   mftransform.h
-   opmapi.h
-   wmcodecdsp.h
-   wmcontainer.h

## <a name="libraries"></a>Bibliotheken

-   dxva2.lib
-   evr.lib
-   mf.lib
-   mfplat.lib
-   mfplay.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="library-changes-in-windows-7"></a>Bibliotheksänderungen in Windows 7

Ab Version Windows 7 werden bestimmte Media Foundation aus anderen DLL-Dateien als frühere Versionen exportiert.

Diese Änderungen wirken sich auf die folgenden LIB-Dateien aus:

-   evr.lib
-   mf.lib
-   mfplat.lib

Eine Anwendung, die eine dieser Funktionen verwendet, muss abhängig von der SDK-Version und der Zielplattform mit einem anderen Satz von LIB-Dateien verknüpfen.




| SDK-Version | Bibliotheken | 
|-------------|-----------|
| Windows SDK für Windows Vista<br /> Windows SDK für Windows Server 2008<br /> | evr.lib<br /> mf.lib<br /> mfplat.lib<br /> | 
| Windows SDK für Windows 7 | Wenn sich die Zielplattform Windows Vista oder Windows Server 2008 befindet, verknüpfen Sie die folgenden Bibliotheken:<br /><ul><li>evr_vista.lib</li><li>mf_vista.lib</li><li>mfplat_vista.lib</li></ul>Wenn die Zielplattform Windows 7 oder höher ist, verknüpfen Sie die folgenden Bibliotheken:<br /><ul><li>evr.lib</li><li>mf.lib</li><li>mfplat.lib</li></ul> | 




 

## <a name="additional-info-on-helper-functions"></a>Zusätzliche Informationen zu Hilfsfunktionen

Der Windows 8 MFPlat.dll ist eine Komponente des Microsoft Windows Betriebssystems. Es verfügt über mehrere Funktionen, die im Modul enthalten sind.

MFPlat implementiert Hilfsfunktionen für Low-Level-Speicherzuordnung, Vorgangsplanung von FIFOs und Win32-Dateizugriffsabstraktionsabstraktion. Um genauer zu sein, bietet sie Unterstützung für Folgendes:

-   Zuordnen und Initialisieren von Speicherpuffern (als "Beispiele" bekannt) und Hilfsmodulen, um die Verwaltung ihrer Lebensdauer zu vereinfachen
-   effiziente Funktionen zum Kopieren von Daten für Speicherpuffer
-   Zuordnen und Initialisieren von FIFOs -Vorgängen (als "Ereignisse" bekannt)
-   Implementieren eines einfachen Uhrobjekts
-   Implementieren eines Win32-Datei-Wrappers
-   Zuordnen und Initialisieren von Arrays von Speicherpuffern für CPUs und GPUs

Wenn die [**MFStartup-Methode**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) erfolgreich ist, stellt MFPlat die folgenden Arbeitswarteschlangenfunktionen zur Verfügung:

-   interne Unterstützung von E/A-Elementen (wie vom Win32-Datei-Wrapper und den Socketbibliotheken verwendet)
-   Bereitstellen eines Arrays von Multithreadarbeitswarteschlangen mit Threadprioritätsunterstützung
-   Unterstützen von Arbeitselementen, Timerelementen und Warteelementen durch die Arbeitswarteschlangen

MFPlat bietet Hilfsfunktionen zum Suchen und Erstellen von Medientransformationen und Medienquellen, die im System registriert sind, und zum Erstellen und Bearbeiten von Medientypen, obwohl MFPlat selbst weder die tatsächlichen Medien erstellen noch wieder geben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




