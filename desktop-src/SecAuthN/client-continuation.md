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
# <a name="client-continuation"></a>Client Fortsetzung

Einige Protokolle erfordern mehrere Authentifizierungs Nachrichten. In diesem Fall analysiert der Client die Antwort vom Server und ruft [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) erneut auf, wobei der Fortsetzung Status des vorherigen Aufrufs verwendet wird. Der Client überprüft den Rückgabestatus dieses Aufrufes und kann ggf. erforderlich sein, um bei zusätzlichen Beinen fortzufahren. Er verwendet die Informationen in *poutput* , um eine Nachricht zu erstellen und an den Server zu senden.

 

 
