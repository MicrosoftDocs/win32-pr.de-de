---
description: Wenn der Client die Kommunikation mit einem Server abgeschlossen oder die zusätzlichen Anmeldeinformationen verwendet hat, die an die AcquireCredentialsHandle-Funktion übergeben wurden, muss der Client die FreeCredentialsHandle-Funktion aufrufen.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Beenden einer SSPI-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008268"
---
# <a name="ending-an-sspi-session"></a>Beenden einer SSPI-Sitzung

Nachdem client und server die Kommunikation abgeschlossen haben, rufen beide Seiten die [**DeleteSecurityContext-Funktion**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) mit ihren jeweiligen Kontexthandles auf. Wenn der Client die Kommunikation mit einem Server abgeschlossen oder die zusätzlichen Anmeldeinformationen verwendet hat, die an die [**AcquireCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) übergeben wurden, muss der Client die [**FreeCredentialsHandle-Funktion**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) aufrufen. Wenn der Server heruntergefahren werden kann und bevor die DLL entladen wird, muss der Server **DeleteSecurityContext** aufrufen.

 

 
