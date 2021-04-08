---
description: Einige Protokolle erfordern mehrere Authentifizierungs Nachrichten.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Client Fortsetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863871"
---
# <a name="client-continuation"></a><span data-ttu-id="173db-103">Client Fortsetzung</span><span class="sxs-lookup"><span data-stu-id="173db-103">Client Continuation</span></span>

<span data-ttu-id="173db-104">Einige Protokolle erfordern mehrere Authentifizierungs Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="173db-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="173db-105">In diesem Fall analysiert der Client die Antwort vom Server und ruft [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) erneut auf, wobei der Fortsetzung Status des vorherigen Aufrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="173db-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="173db-106">Der Client überprüft den Rückgabestatus dieses Aufrufes und kann ggf. erforderlich sein, um bei zusätzlichen Beinen fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="173db-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="173db-107">Er verwendet die Informationen in *poutput* , um eine Nachricht zu erstellen und an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="173db-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
