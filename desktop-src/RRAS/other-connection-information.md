---
title: Weitere Verbindungsinformationen
description: Die Member der RASDIALPARAMS-Struktur können auch die folgenden Verbindungsinformationen angeben.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c596dbfb160766283beb9c48a5faf4e8258dcf0361ad7a504188a29207c0500f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789931"
---
# <a name="other-connection-information"></a>Weitere Verbindungsinformationen

Die Member der [**RASDIALPARAMS-Struktur**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) können auch die folgenden Verbindungsinformationen angeben.

-   Eine Telefonnummer, um die Nummer im Telefonbucheintrag zu überschreiben.
-   Eine [](callback-connections.md) Rückruftelefonnummer, die der Remoteserver zurückrufen kann, um die Verbindung herzustellen.
-   Der Name der Remotenetzwerkdomäne, in der die Authentifizierung erfolgen soll.

Für die Rückrufnummer und die Domäne können die [**RASDIALPARAMS-Mitglieder**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) entweder angeben, dass RAS die Informationen im Telefonbucheintrag verwenden soll, oder sie können Informationen bereitstellen, die die Telefonbuchdaten überschreiben.

Ein RAS-Client kann den *lpRasDialExtensions-Parameter* der [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) verwenden, um zu steuern, ob RAS ein Telefonnummernpräfix oder suffix verwendet, das in einem Telefonbucheintrag angegeben ist.

 

 