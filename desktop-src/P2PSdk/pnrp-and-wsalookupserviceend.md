---
description: PNRP verwendet die WSALookupServiceEnd-Funktion, um Folgendes durchzuführen.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP und WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347688"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP und WSALookupServiceEnd

PNRP verwendet die [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) -Funktion, um Folgendes durchzuführen:

-   Beenden einer Abfrage, die in einem vorherigen [ **wsalookupservicebegin** -aufrufen initiiert wurde](winsock-nsp-reference-links.md)
-   Aufheben der Blockierung eines [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Aufrufes zum Abbrechen der Suche

Ein [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) -Aufrufe beendet eine Abfrage und bereinigt den Kontext. Das von einem **wsalookupservicebegin** -Befehl erhaltene Handle muss als Parameter an **WSALookupServiceEnd** übergeben werden.

Weitere Informationen zu PNRP und der [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Funktion finden Sie unter [PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP-NSP-Fehler Codes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



