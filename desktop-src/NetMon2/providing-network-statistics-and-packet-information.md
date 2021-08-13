---
description: Der Netzwerkpaketanbieter (Network Packet Provider, NPP) ist eine DLL, die mit dem Netzwerkmonitor-Treiber kommuniziert und Netzwerkstatistiken und Paketdaten bereitstellt.
ms.assetid: ee258bf7-7894-458d-b418-57a19ac985f2
title: Bereitstellen von Netzwerkstatistiken und Paketinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb3165c56d3ca9b2fc06dd7162010b8a8813b59b1e08167c8c3229c2642bc4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339530"
---
# <a name="providing-network-statistics-and-packet-information"></a>Bereitstellen von Netzwerkstatistiken und Paketinformationen

Der Netzwerkpaketanbieter (Network Packet Provider, NPP) ist eine DLL, die mit dem Netzwerkmonitor-Treiber kommuniziert und Netzwerkstatistiken und Paketdaten bereitstellt.

Die gängigsten Möglichkeiten zur Verwendung des NPP sind:

-   Netzwerkstatistiken.
-   Frames, die in Echtzeit an die Anwendung übergeben werden.
-   Auf Pakete kann erst zugegriffen werden, nachdem die Erfassung beendet wurde.

Dieser Abschnitt schließt folgende Themen ein:

-   [Auswählen einer NIC](selecting-a-nic-using-getnppblobfromui.md)
-   [Verwenden von GetNPPBlobTable](using-getnppblobtable.md)

 

 



