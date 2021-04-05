---
description: Wenn die Kommunikation des Clients mit einem beliebigen Server abgeschlossen ist oder die zusätzlichen Anmelde Informationen, die an die AcquireCredentialsHandle-Funktion weitergegeben wurden, nicht mehr verwendet werden, muss der Client die freecredentialshandle-Funktion aufrufen.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Beenden einer SSPI-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750929"
---
# <a name="ending-an-sspi-session"></a>Beenden einer SSPI-Sitzung

Nachdem die Kommunikation zwischen Client und Server abgeschlossen ist, wird die [**Delta Context**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) -Funktion von beiden Seiten mit den entsprechenden Kontext Handles aufgerufen. Wenn die Kommunikation des Clients mit einem beliebigen Server abgeschlossen ist oder die zusätzlichen Anmelde Informationen, die an die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion weitergegeben wurden, nicht mehr verwendet werden, muss der Client die [**freecredentialshandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen. Wenn der Server zum Herunterfahren und vor dem Entladen der dll bereit ist, muss der Server " **Delta Context**" aufruft.

 

 
