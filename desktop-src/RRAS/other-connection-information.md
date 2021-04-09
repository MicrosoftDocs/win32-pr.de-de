---
title: Weitere Verbindungsinformationen
description: Die Member der rasdialparameams-Struktur können auch die folgenden Verbindungsinformationen angeben.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948848"
---
# <a name="other-connection-information"></a>Weitere Verbindungsinformationen

Die Member der [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) -Struktur können auch die folgenden Verbindungsinformationen angeben.

-   Eine Telefonnummer, mit der die Nummer im Telefonbucheintrag überschrieben werden soll.
-   Eine [Rückruf](callback-connections.md) Telefonnummer, die vom Remote Server aufgerufen werden kann, um die Verbindung herzustellen.
-   Der Name der Remote Netzwerk Domäne, in der die Authentifizierung erfolgen soll.

Für die Rückrufnummer und die Domäne können die Mitglieder des [**rasdialparamemes**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) entweder angeben, dass RAS die Informationen im Telefonbucheintrag verwenden soll, oder es können Informationen bereitgestellt werden, die die Telefonbuchdaten überschreiben.

Ein RAS-Client kann den *lprasdialextensions* -Parameter der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Funktion verwenden, um zu steuern, ob RAS das in einem Telefonbucheintrag angegebene Telefonnummern Präfix oder-Suffix verwendet.

 

 