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
# <a name="ndf-diagnostics-example"></a>NDF-Diagnose Beispiel

Im folgenden Beispiel wird gezeigt, wie die NDF-Benutzeroberfläche gestartet und die Konnektivität mit der Website diagnostiziert wird https://www.microsoft.com .


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



Die NDF-Benutzeroberfläche kann als modales Fenster gestartet werden. Zu diesem Zweck ändern Sie den zweiten Parameter von [**ndfexecutediagnose**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) von **null** in das Handle (HWND) des übergeordneten Fensters.

Dieses Beispiel kann so geändert werden, dass andere Netzwerk Bereiche diagnostiziert werden. Ersetzen Sie hierzu den [**ndfkreatewebincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) -Befehl durch eine der anderen incidenterstellungs-Funktionen, wie z. b. [**ndfkreatednsincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) oder [**ndfkreatewinsockincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ndfcloseincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**Ndfkreatewebincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**Ndfexecutediagnose**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




