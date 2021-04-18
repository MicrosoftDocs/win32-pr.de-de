---
description: Ein Erfassungs Filter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten werden sollen und welche Frames ignoriert werden sollen.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informationen zu Erfassungs Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359021"
---
# <a name="about-capture-filters"></a>Informationen zu Erfassungs Filtern

Ein Erfassungs Filter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten werden sollen und welche Frames ignoriert werden sollen. Der Vorteil der Festlegung eines Erfassungs Filters ist eine höhere Effizienz. Sie müssen keine aufgezeichneten Frames untersuchen. Diese werden vom Netzwerkmonitor Treiber untersucht. Durch diese Vorgehensweise wird das Kopieren von Frames vermieden

## <a name="capture-filter-structure"></a>Erfassungs Filter Struktur

Erfassungs Filter bestehen aus drei Elementen:

-   ETYPE/SAP-Einstellungen
-   Adresse
-   Muster Übereinstimmung

In dieser Weise Werten diese Elemente logisch aus, welche Frames während der Ausführung einer NPP-Anwendung eingeschlossen oder ausgeschlossen werden sollen. Der Erfassungs Filter liefert komplexe Übereinstimmungen und Ausschlüsse von Frame Elementen für die NPP-Anwendung.

Netzwerkmonitor implementiert den Erfassungs Filter über eine Datenstruktur ( [**capturefilter**](the-capturefilter-structure.md)), die an den NPP weitergegeben und beim Start der Erfassung an den Netzwerkmonitor Treiber weitergeleitet wird.

Weitere Informationen zu NPP-Vorgängen und BLOB-Funktionen finden Sie unter [Netzwerk Paketanbieter](network-packet-providers.md) und [Netzwerkmonitor BLOBs](network-monitor-blobs.md).

 

 



