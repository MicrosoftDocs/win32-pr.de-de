---
description: Ein Dienstanbieter kann extern generierte Telefonnummern angeben, indem er Member der LINECALLINFO-Struktur festlegt, wenn die TSPI- \_ Funktion linegetcallinfo verarbeitet wird.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Extern generierte Telefonnummern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751616"
---
# <a name="externally-generated-phone-numbers"></a>Extern generierte Telefonnummern

Ein Dienstanbieter kann extern generierte Telefonnummern (d. h. Zahlen für ausgehende Aufrufe, die extern auf dem Computer generiert werden) anzeigen, indem er die Elemente **displayableaddress**, **calledparty** oder [comment](./comment-ovr.md) in der [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) -Struktur festlegt, wenn die [**TSPI-Funktion \_ linegetcallinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) verarbeitet wird. Wenn TAPI seine eigenen Daten für diese Member nicht gespeichert hat, bleiben die vom Dienstanbieter festgelegten Daten unverändert. Wenn TAPI über zwischengespeicherte Daten für diese Member verfügt, fügt TAPI seinen Text am Ende des Variablen Teils der **LINECALLINFO** -Struktur hinzu und überschreibt die Größe und den Offset, die der Dienstanbieter in den Fixed-Teil eingefügt hat.

Ein Dienstanbieter kann auch eine ausgehende Nummer in das **calledid** -Element kopieren. Daher sollten Protokollierungs Anwendungen den **calledid** -Member auf ausgehende Aufrufe überprüfen, wenn die Member " **displayableaddress** " und " **calledparty** " leer sind.

 

 
