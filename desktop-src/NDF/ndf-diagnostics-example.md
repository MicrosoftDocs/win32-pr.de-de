---
title: NDF-Diagnosebeispiel
description: Das folgende Beispiel zeigt, wie Sie die NDF-Benutzeroberfläche starten und die Konnektivität mit der Website http ://www.microsoft.com diagnostizieren.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802370"
---
# <a name="ndf-diagnostics-example"></a>NDF-Diagnosebeispiel

Das folgende Beispiel zeigt, wie sie die NDF-Benutzeroberfläche starten und die Konnektivität mit der Website diagnostizieren. https://www.microsoft.com


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



Die NDF-Benutzeroberfläche kann als modales Fenster gestartet werden. Ändern Sie hierzu den zweiten Parameter von [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) von **NULL** in das Handle (HWND) des übergeordneten Fensters.

Dieses Beispiel kann geändert werden, um andere Netzwerkbereiche zu diagnostizieren. Ersetzen Sie dazu den [**NdfCreateWebIncident-Aufruf**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) durch eine der anderen Funktionen zum Erstellen von Vorfällen, z. B. [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) oder [**NdfCreateWinSockIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




