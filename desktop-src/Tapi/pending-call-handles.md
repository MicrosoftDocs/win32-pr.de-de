---
description: Ein Dienstanbieter ist erforderlich, um einen oder mehrere Aufruf Handles (Variablen des Typs hdrvcall) zu erstellen, wenn TAPI eine der folgenden Funktionen aufruft.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Ausstehende Rückruf Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345698"
---
# <a name="pending-call-handles"></a>Ausstehende Rückruf Handles

Ein Dienstanbieter ist erforderlich, um einen oder mehrere Aufruf Handles (Variablen des Typs [hdrvcall)](hdrvline.md)zu erstellen, wenn TAPI eine dieser Funktionen aufruft: [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ linecompletetransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI \_ lineforward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linepickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ lineprepareaddumconference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ linesetupconference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)und [**TSPI \_ lineunpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Wenn ein Dienstanbieter einen solchen-Befehl empfängt, muss der Dienstanbieter die von TAPI angegebene Variable auf den Wert des Handles festlegen, bevor der-Befehl zurückgegeben wird. TAPI betrachtet dieses "ausstehende Telefon Handle" als vorläufig gültig. Wenn der Dienstanbieter den-Aufrufs tatsächlich erstellt, muss er den asynchronen [**\_ Abschluss**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückruf aufrufen, um das Handle formal zu validieren.

Wenn TAPI die [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) -Funktion aufruft, bevor der Dienstanbieter ein ausstehendes Aufruf handle formal überprüft, muss der Dienstanbieter alle weiteren mit dem Aufruf handle verknüpften Verarbeitungsschritte beenden und die asynchrone [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückruffunktion mithilfe des Fehler Werts lineerr \_ operationfailed aufrufen.

 

 
