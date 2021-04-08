---
title: Behandeln von Server Anwendungsfehlern
description: Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet hat, sollte die Anwendung 200 zurückgeben.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707854"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="7eecf-103">Behandeln von Server Anwendungsfehlern</span><span class="sxs-lookup"><span data-stu-id="7eecf-103">Handling Server Application Errors</span></span>

<span data-ttu-id="7eecf-104">Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet hat, sollte die Anwendung 200 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7eecf-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="7eecf-105">Wenn die Anwendung nicht 200 zurückgibt, verwendet der BITS-Client den Fehlercode, um zu ermitteln, ob der Fehler ein vorübergehender Fehler oder ein schwerwiegender Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="7eecf-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="7eecf-106">Alle 3xx-Fehlercodes sind vorübergehende Fehler außer 300-305 und 307, bei denen es sich um schwerwiegende Fehler handelt.</span><span class="sxs-lookup"><span data-stu-id="7eecf-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="7eecf-107">Alle 4xx-Fehlercodes sind schwerwiegende Fehler, außer 408 und 409, bei denen es sich um vorübergehende Fehler handelt.</span><span class="sxs-lookup"><span data-stu-id="7eecf-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="7eecf-108">Alle 5xx-Fehlercodes sind vorübergehende Fehler außer 501 und 505, bei denen es sich um schwerwiegende Fehler handelt.</span><span class="sxs-lookup"><span data-stu-id="7eecf-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="7eecf-109">Alle anderen HTTP-Codes werden als vorübergehende Fehler betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7eecf-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="7eecf-110">Beachten Sie, dass der Fehlercode 403 der einzige Fehlercode ist, der verhindert, dass Bits die Uploaddatei erneut an die Serveranwendung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7eecf-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="7eecf-111">Um den Fehler abzurufen, rufen Sie die [**ibackgroundcopyerror:: getError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7eecf-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="7eecf-112">Der Fehler Kontext ist eine BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7eecf-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




