---
title: Benutzerauthentifizierungsinformationen
description: Der Ras-Verbindungs-Manager-Dienst auf dem Clientcomputer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remotecomputer.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f347cd9f42106619f2558bdcbc677c961b4fae749912c92dd32ac2c8096f6fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127810"
---
# <a name="user-authentication-information"></a>Benutzerauthentifizierungsinformationen

Der Ras-Verbindungs-Manager-Dienst auf dem Clientcomputer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remotecomputer. Bevor eine Verbindung hergestellt wird, verwendet der Remoteserver diese Informationen, um den Benutzer zu authentifizieren. Standardmäßig sendet die Remotezugriffs-Verbindungs-Manager den Benutzernamen und das Kennwort des aktuell angemeldeten Benutzers. Der RAS-Client kann die im [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) angegebene [**RASDIALPARAMS-Struktur**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) verwenden, um einen anderen Benutzernamen und ein anderes Kennwort anzugeben.

Wenn der Remoteserver den Benutzer nicht mit den angegebenen Informationen authentifizieren kann, kann er zulassen, dass der Verbindungsvorgang in einen [angehaltenen Zustand](paused-states.md) versetzt wird, damit der RAS-Client unterschiedliche Authentifizierungsdaten vom Benutzer sammeln kann.

 

 