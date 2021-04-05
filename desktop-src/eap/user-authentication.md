---
title: Benutzerauthentifizierung
description: Das Authentifizierungsprotokoll selbst kann den Benutzer über das geschützte EAP (PEAP) authentifizieren.
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719571"
---
# <a name="user-authentication"></a>Benutzerauthentifizierung

Das Authentifizierungsprotokoll selbst kann den Benutzer über das geschützte EAP (PEAP) authentifizieren. Es gibt auch zwei Authentifizierungs Anbieter, die in das Betriebssystem integriert sind: Windows-Domänen Authentifizierung (Zugriff über Verzeichnisdienste) und RAS (Remote Access Dial-in User Service).

Wenn RADIUS der Authentifizierungs Anbieter ist, wird das EAP-Plug-in auf dem RADIUS-Server und nicht auf dem drahtlos Zugriffspunkt-Server (z. b. einem RAS-Server) installiert. Der AP-Server übergibt EAP-Pakete direkt vom Client an den Authentifizierungsdienst auf dem RADIUS-Server. Der AP-Server verarbeitet keine der Informationen in den EAP-Paketen, er muss jedoch die vom serverseitigen, vollständigen PEAP generierten Verschlüsselungsschlüssel (256 Bit) akzeptieren, um die sichere Verbindung zu erstellen.

 

 




