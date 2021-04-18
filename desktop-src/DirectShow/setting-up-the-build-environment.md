---
description: Entwickeln von DirectShow-Anwendungen
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Entwickeln von DirectShow-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338850"
---
# <a name="building-directshow-applications"></a>Entwickeln von DirectShow-Anwendungen

In diesem Thema werden die Header und Bibliotheken beschrieben, die zum Erstellen von DirectShow-Anwendungen erforderlich sind.

Die neuesten DirectShow-Header und-Bibliotheken sind im [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)verfügbar.

## <a name="header-files"></a>Headerdateien

Alle DirectShow-Anwendungen verwenden die in der folgenden Tabelle gezeigte Header Datei.



| Headerdatei | Erforderlich für                 |
|-------------|------------------------------|
| DShow. h     | Alle DirectShow-Anwendungen. |



 

Einige DirectShow-Schnittstellen erfordern zusätzliche Header Dateien. Diese Anforderungen sind in der Schnittstellenreferenz aufgeführt.

## <a name="library-files"></a>Bibliotheksdateien

DirectShow verwendet die statischen Bibliotheksdateien, die in der folgenden Tabelle aufgeführt sind.



| Bibliotheksdatei | BESCHREIBUNG                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| "" "" ". Lib" | Exportiert Klassen Bezeichner (CLSIDs) und Schnittstellen Bezeichner (IIDs).                                                           |
| Quarz. lib   | Exportiert die [**amgeterrortext**](/windows/win32/api/errors/nf-errors-amgeterrortexta) -Funktion. Wenn Sie diese Funktion nicht aufzurufen, ist diese Bibliothek nicht erforderlich. |



 

Verwenden Sie die gleichen lib-Dateien für Debug-und Releasebuilds.

## <a name="filter-base-classes"></a>Filtern von Basisklassen

Der Windows SDK stellt eine Reihe von C++-Klassen bereit, die empfohlen werden, wenn Sie einen benutzerdefinierten DirectShow-Filter schreiben. Diese Klassen werden als Beispielcode bereitgestellt, der in einer statischen Bibliothek kompiliert werden kann. Weitere Informationen finden Sie unter [DirectShow-Basisklassen](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>Verteilbare DLLs

Für DirectShow-Anwendungen, die für Windows XP mit Service Pack 2 (SP2) und höher geschrieben wurden, müssen keine DirectShow-DLLs neu verteilt werden.

Für Windows XP mit Service Pack 1 (SP1) und früher sind verteilbare DirectShow-DLLs über das Microsoft DirectX SDK verfügbar. Die neueste Version dieser DLLs ist Version 9.0 c. Es ist keine weitere Entwicklung dieser verteilbaren DLLs geplant. Windows XP mit Service Pack 2 (SP2) enthält die c-DLLs der Version 9.0.

Die redstributable-Pakete enthalten die folgenden DLLs:

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen von DirectShow-Filtern](building-directshow-filters.md)
</dt> </dl>

 

 
