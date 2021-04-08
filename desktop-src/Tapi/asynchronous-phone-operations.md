---
description: Es sind neun asynchrone Vorgänge im Zusammenhang mit Smartphones vorhanden.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Asynchrone Telefon Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866599"
---
# <a name="asynchronous-phone-operations"></a>Asynchrone Telefon Vorgänge

Es sind neun asynchrone Vorgänge im Zusammenhang mit Smartphones vorhanden. Diese werden von der [**TSPI \_ phonedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI \_ phonesetbuttoninfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI \_ phonesetdata**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**TSPI \_ phonesetdisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_ phonesetcount**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI \_ phonesethookswitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI \_ phonesetlamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI \_ phonesetring**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)und [**TSPI \_ phonesetvolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) -Funktionen initiiert. Wenn eine Anwendung die TAPI [**phoneclose**](/windows/win32/api/tapi/nf-tapi-phoneclose) -Funktion aufruft und über das einzige Handle für das Telefon verfügt, ruft TAPI die [**TSPI \_ phoneclose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) -Funktion auf, um den Dienstanbieter anzuweisen, die asynchronen Vorgänge zu beenden und die Abschluss Prozedur-Rückruffunktion nach Bedarf aufzurufen. [*\_*](/windows/win32/api/tspi/nc-tspi-async_completion) Wenn die Anwendung nicht über das einzige Handle für das Telefon verfügt, empfängt der Dienstanbieter keine Benachrichtigung über die Anforderung, und alle ausstehenden asynchronen Vorgänge bleiben aktiv.

 

 
