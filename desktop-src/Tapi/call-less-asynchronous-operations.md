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
# <a name="call-less-asynchronous-operations"></a><span data-ttu-id="17df6-103">Aufrufe ohne asynchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="17df6-103">Call-less Asynchronous Operations</span></span>

<span data-ttu-id="17df6-104">Es gibt fünf asynchrone Vorgänge, die nicht mit einem bestimmten-Befehl verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="17df6-104">There are five asynchronous operations that are not related to any particular call.</span></span> <span data-ttu-id="17df6-105">Die Funktionen "TAPI 2. x [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)", " [**linedevspecificfeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)", " [**lineforward**](/windows/win32/api/tapi/nf-tapi-lineforward)", " [**linesetterminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)" und " [**lineuncompletecall"**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) initiieren diese Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="17df6-105">The TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal), and [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) functions initiate these operations.</span></span> <span data-ttu-id="17df6-106">Wenn eine Anwendung einen dieser asynchronen Vorgänge initiiert und [**lineclose**](/windows/win32/api/tapi/nf-tapi-lineclose)aufruft, kann der Dienstanbieter nicht darauf hinweisen, dass die Anwendung die Funktion abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="17df6-106">If an application initiates one of these asynchronous operations and calls [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), the service provider may receive no indication that the application has abandoned the function.</span></span> <span data-ttu-id="17df6-107">Dies kann vorkommen, wenn die Anwendung nicht die einzige Anwendung war, in der die Zeile geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="17df6-107">This can occur if the application was not the only application to have the line open.</span></span> <span data-ttu-id="17df6-108">Wenn die Anwendung **lineclose** aufruft, wobei eine dieser Vorgänge aussteht, und es sich um die einzige Anwendung mit einem Handle der Zeile handelt, ruft TAPI die [**TSPI \_ lineclose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) -Funktion auf, und der Dienstanbieter sollte den asynchronen Vorgang beenden, wobei die Abschluss Prozedur-Rückruffunktion für jeden derartigen ausstehenden Vorgang mit dem lineerr [*\_*](/windows/win32/api/tspi/nc-tspi-async_completion) \_ operationfailed-Fehlerwert aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="17df6-108">If the application calls **lineClose** with one of these operations pending, and it is the only application with a handle to the line, TAPI calls the [**TSPI\_lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) function and the service provider should terminate the asynchronous operation, calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function for each such outstanding operation with the LINEERR\_OPERATIONFAILED error value.</span></span>

 

 
