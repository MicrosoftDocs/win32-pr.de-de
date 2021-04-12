---
description: Es gibt fünf asynchrone Vorgänge, die nicht mit einem bestimmten-Befehl verknüpft sind.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Aufrufe ohne asynchrone Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345698"
---
# <a name="call-less-asynchronous-operations"></a>Aufrufe ohne asynchrone Vorgänge

Es gibt fünf asynchrone Vorgänge, die nicht mit einem bestimmten-Befehl verknüpft sind. Die Funktionen "TAPI 2. x [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)", " [**linedevspecificfeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)", " [**lineforward**](/windows/win32/api/tapi/nf-tapi-lineforward)", " [**linesetterminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)" und " [**lineuncompletecall"**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) initiieren diese Vorgänge. Wenn eine Anwendung einen dieser asynchronen Vorgänge initiiert und [**lineclose**](/windows/win32/api/tapi/nf-tapi-lineclose)aufruft, kann der Dienstanbieter nicht darauf hinweisen, dass die Anwendung die Funktion abgebrochen hat. Dies kann vorkommen, wenn die Anwendung nicht die einzige Anwendung war, in der die Zeile geöffnet werden konnte. Wenn die Anwendung **lineclose** aufruft, wobei eine dieser Vorgänge aussteht, und es sich um die einzige Anwendung mit einem Handle der Zeile handelt, ruft TAPI die [**TSPI \_ lineclose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) -Funktion auf, und der Dienstanbieter sollte den asynchronen Vorgang beenden, wobei die Abschluss Prozedur-Rückruffunktion für jeden derartigen ausstehenden Vorgang mit dem lineerr [*\_*](/windows/win32/api/tspi/nc-tspi-async_completion) \_ operationfailed-Fehlerwert aufgerufen wird.

 

 
