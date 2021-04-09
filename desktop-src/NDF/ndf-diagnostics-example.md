---
title: NDF-Diagnose Beispiel
description: Im folgenden Beispiel wird gezeigt, wie Sie die NDF-Benutzeroberfläche starten und die Konnektivität mit der Website http//www.Microsoft.com diagnostizieren.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036822"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="b710b-103">NDF-Diagnose Beispiel</span><span class="sxs-lookup"><span data-stu-id="b710b-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="b710b-104">Im folgenden Beispiel wird gezeigt, wie die NDF-Benutzeroberfläche gestartet und die Konnektivität mit der Website diagnostiziert wird https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b710b-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="b710b-105">Die NDF-Benutzeroberfläche kann als modales Fenster gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b710b-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="b710b-106">Zu diesem Zweck ändern Sie den zweiten Parameter von [**ndfexecutediagnose**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) von **null** in das Handle (HWND) des übergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="b710b-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="b710b-107">Dieses Beispiel kann so geändert werden, dass andere Netzwerk Bereiche diagnostiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b710b-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="b710b-108">Ersetzen Sie hierzu den [**ndfkreatewebincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) -Befehl durch eine der anderen incidenterstellungs-Funktionen, wie z. b. [**ndfkreatednsincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) oder [**ndfkreatewinsockincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="b710b-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b710b-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b710b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b710b-110">**Ndfcloseincident**</span><span class="sxs-lookup"><span data-stu-id="b710b-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="b710b-111">**Ndfkreatewebincident**</span><span class="sxs-lookup"><span data-stu-id="b710b-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="b710b-112">**Ndfexecutediagnose**</span><span class="sxs-lookup"><span data-stu-id="b710b-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




