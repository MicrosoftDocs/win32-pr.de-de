---
title: Benutzerauthentifizierung
description: Das Authentifizierungsprotokoll selbst kann den Benutzer über protected EAP (PEAP) authentifizieren.
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3f5d377163f2519d97de847d8d14b5bd96925577a8133988adf8fbf950b283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978370"
---
# <a name="user-authentication"></a>Benutzerauthentifizierung

Das Authentifizierungsprotokoll selbst kann den Benutzer über protected EAP (PEAP) authentifizieren. Es gibt auch zwei Authentifizierungsanbieter, die in das Betriebssystem integriert sind: Windows Domänenauthentifizierung (Zugriff über Verzeichnisdienste) und REMOTE ACCESS DIAL-In User Service (RADIUS).

Wenn RADIUS der Authentifizierungsanbieter ist, wird das EAP-Plug-In auf dem RADIUS-Server und nicht auf dem DRAHTLOSEN Zugriffspunktserver (z. B. einem RAS-Server) installiert. Der AP-Server übergibt EAP-Pakete direkt vom Client an den Authentifizierungsdienst auf dem RADIUS-Server. Der AP-Server verarbeitet keine der Informationen in den EAP-Paketen, muss jedoch die serverseitigen, vollständigen PeAP-verschlüsselungsschlüssel (256 Bit) akzeptieren, um die sichere Verbindung herzustellen.

 

 




