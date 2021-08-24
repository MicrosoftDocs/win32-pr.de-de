---
description: Ein Dienstanbieter ist erforderlich, um mindestens einen Aufrufhandles (Variablen vom Typ HDRVCALL) zu erstellen, wenn TAPI eine der folgenden Funktionen aufruft.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Ausstehende Aufrufhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518589"
---
# <a name="pending-call-handles"></a>Ausstehende Aufrufhandles

Ein Dienstanbieter muss mindestens einen Aufrufhandles (Variablen vom Typ [HDRVCALL](hdrvline.md)) erstellen, wenn TAPI eine der folgenden Funktionen aufruft: [**TSPI \_ lineMakeCall,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) [**TSPI \_ lineCompleteTransfer,**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer) [**TSPI \_ lineForward,**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward) [**TSPI \_ linePickup,**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup) [**TSPI \_ linePrepareAddToConference,**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference) [**TSPI \_ lineSetupConference,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)und [**TSPI \_ lineUnpark.**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark) Wenn ein Dienstanbieter einen solchen Aufruf empfängt, muss der Dienstanbieter die von TAPI bereitgestellte Variable auf den Wert des Handle festlegen, bevor er vom Aufruf zurückkehrt. TAPI betrachtet dieses "ausstehende Anrufhandli" als vorläufig gültig. Wenn der Dienstanbieter den Aufruf tatsächlich erstellt, muss er den [**ASYNC \_ COMPLETION-Rückruf**](/windows/win32/api/tspi/nc-tspi-async_completion) aufrufen, um das Handle formal zu überprüfen.

Wenn TAPI die [**TSPI-LineCloseCall-Funktion \_**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) aufruft, bevor der Dienstanbieter ein ausstehendes Aufrufhandl formal überprüft, muss der Dienstanbieter die weitere Verarbeitung des Aufrufhandls beenden und die [**ASYNC \_ COMPLETION-Rückruffunktion**](/windows/win32/api/tspi/nc-tspi-async_completion) mithilfe des Fehlerwerts LINEERR \_ OPERATIONFAILED aufrufen.

 

 
