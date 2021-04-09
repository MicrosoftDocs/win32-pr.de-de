---
title: Informationen zur Benutzerauthentifizierung
description: Der RAS-Verbindungs-Manager-Dienst auf dem Client Computer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remote Computer.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858291"
---
# <a name="user-authentication-information"></a>Informationen zur Benutzerauthentifizierung

Der RAS-Verbindungs-Manager-Dienst auf dem Client Computer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remote Computer. Bevor eine Verbindung hergestellt wird, werden diese Informationen vom Remote Server zum Authentifizieren des Benutzers verwendet. Standardmäßig sendet der RAS-Verbindungs-Manager den Benutzernamen und das Kennwort des aktuell angemeldeten Benutzers. Der RAS-Client kann die im Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " angegebene Struktur " [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) " verwenden, um einen anderen Benutzernamen und ein anderes Kennwort anzugeben.

Wenn der Remote Server den Benutzer nicht mit den angegebenen Informationen authentifizieren kann, kann der Verbindungsvorgang in einen [angehaltenen Zustand](paused-states.md) versetzt werden, damit der RAS-Client verschiedene Authentifizierungsdaten des Benutzers erfassen kann.

 

 