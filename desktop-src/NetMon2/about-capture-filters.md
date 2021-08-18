---
description: Ein Erfassungsfilter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor-Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten und welche Frames ignoriert werden sollen.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informationen zu Erfassungsfiltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0d1eee25915c30b8ddffc475545cbd7f7d04d0fdcecf4119480b737980cd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911360"
---
# <a name="about-capture-filters"></a>Informationen zu Erfassungsfiltern

Ein Erfassungsfilter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor-Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten und welche Frames ignoriert werden sollen. Das Festlegen eines Erfassungsfilters hat den Vorteil einer höheren Effizienz. Erfasste Frames müssen nicht untersucht werden. der Netzwerkmonitor Treiber überprüft sie. Durch diesen Ansatz wird das Kopieren von Frames vermieden, was einen Speichernutzungsvorteil bietet.

## <a name="capture-filter-structure"></a>Erfassungsfilterstruktur

Erfassungsfilter bestehen aus drei Elementen:

-   Etype-/SAP-Einstellungen
-   Adresse
-   Muster übereinstimmung

Zusammen werten diese Elemente logisch aus, welche Frames während des Betriebs einer NPP-Anwendung eingeschlossen oder ausgeschlossen werden sollen. Der Erfassungsfilter stellt komplexe Übereinstimmungen und Ausschlüsse von Frameelementen für die NPP-Anwendung bereit.

Netzwerkmonitor implementiert den Erfassungsfilter über eine [**Datenstruktur( CAPTUREFILTER**](the-capturefilter-structure.md)), die an das NPP übergeben und dann beim Start der Erfassung an den Netzwerkmonitor-Treiber übergeben wird.

Weitere Informationen zu NPP-Vorgängen und BLOB-Funktionen finden Sie unter [Netzwerkpaketanbieter](network-packet-providers.md) und [Netzwerkmonitor BLOBS.](network-monitor-blobs.md)

 

 



