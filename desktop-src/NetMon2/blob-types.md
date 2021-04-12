---
description: Netzwerkmonitor verwendet drei Typen von BLOB (Binary Large Objects) zum auswählen und Verbinden von Netzwerkschnittstellenkarten (NICs), zum Erfassen von Daten und zum Bearbeiten von NPP-Daten.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: BLOB-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218334"
---
# <a name="blob-types"></a>BLOB-Typen

Netzwerkmonitor verwendet drei Typen von BLOB (Binary Large Objects) zum auswählen und Verbinden von Netzwerkschnittstellenkarten (NICs), zum Erfassen von Daten und zum Bearbeiten von NPP-Daten.

## <a name="npp-blob"></a>NPP-BLOB

Anwendungen verwenden NPP-blobfunktionen, um über eine NPP eine Verbindung mit einer bestimmten NIC herzustellen. (Die Anwendung stellt die Verbindung mit einem aufzurufenden Aufrufen von " **anatenppinterface** " und Standortdaten im NPP-BLOB her.) Eine Anwendung kann Ihre Konfigurationsdaten auch im NPP-BLOB speichern, um den NPP zu konfigurieren. Außerdem ist es nicht erforderlich, dass eine Anwendung, die das NPP-BLOB speichert, den Finder durchläuft, um das BLOB wiederzuverwenden.

## <a name="filter-blob"></a>Filterblob

Ein filterblob enthält Anwendungs definierte Kriterien, die Sie verwenden können, um eine NPP und eine NIC auszuwählen. Beispielsweise kann eine Anwendung eine bestimmte NIC, nur Ethernet-Karten oder Karten anfordern, die eine bestimmte Frame Erfassungs Rate unterstützen.

## <a name="special-blob"></a>Spezielles BLOB

Wenn ein NPP zusätzliche Daten benötigt, bevor er ein NPP-BLOB an eine Anwendung zurückgeben kann, verwendet der NPP ein spezielles BLOB. In den meisten Fällen benötigt die Anwendung keine speziellen blobwerte, sodass Sie nicht an eine Anwendung zurückgegeben werden, es sei denn, ein bestimmtes Flag wird in einem Funktions Aufrufsatz festgelegt. Ein Remote-NPP verwendet beispielsweise ein spezielles BLOB, da zum Herstellen einer Verbindung ein Pfadname erforderlich ist. Eine Anwendung, die ein Remote-NPP-spezielles BLOB empfängt, kann die Zeichenfolge hinzufügen und zum Finder zurückkehren, um eine NPP-BLOB-Tabelle abzurufen. Weitere Informationen finden Sie unter [Special BLOB Entries](special-blob-entries.md).

 

 



