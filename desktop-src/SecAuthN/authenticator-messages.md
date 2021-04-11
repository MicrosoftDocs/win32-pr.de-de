---
description: In einem einfachen Protokoll, das die Authentifizierung mit geheimem Schlüssel verwendet, zeigt ein Client eine Authentifikator-Nachricht in Form von Informationen an, die im Sitzungsschlüssel verschlüsselt sind.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Authenticator-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216540"
---
# <a name="authenticator-messages"></a>Authenticator-Meldungen

In einem einfachen Protokoll, das die Authentifizierung mit geheimem Schlüssel verwendet, zeigt ein Client eine Authentifikator-Nachricht in Form von Informationen an, die im [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly)verschlüsselt sind. Die Informationen in der Authenticator-Nachricht müssen bei jeder Ausführung des Authentifizierungs Protokolls anders sein, oder eine verschlüsselte authentifikatornachricht kann von einer nicht autorisierten Entität wieder verwendet werden.

Beim Empfang der Authentifikator-Nachricht entschlüsselt der Server ihn und kann über den Inhalt der entschlüsselten Nachricht erkennen, ob die Entschlüsselung erfolgreich war. Wenn die entschlüsselte Nachricht nicht giberish ist, weiß der Server, dass der Client, der die Authenticator-Nachricht präsentiert, den richtigen Schlüssel zum Verschlüsseln der Nachricht verwendet hat. Nur zwei Entitäten haben Zugriff auf den [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) . wenn es sich bei dem Server um einen handelt, muss der Client, der die Authentifikator-Nachricht verschlüsselt hat, der andere sein.

Bei der gegenseitigen Authentifizierung wird ein ähnliches Protokoll ausgeführt. Der Server extrahiert einen Teil der Informationen aus der entschlüsselten, ursprünglichen authentifikatornachricht, verschlüsselt ihn mit dem gemeinsamen Sitzungsschlüssel und sendet die verschlüsselte Nachricht an den Client. Der Client entschlüsselt die Nachricht und vergleicht das Ergebnis mit dem ursprünglichen. Wenn die entschlüsselte Nachricht mit dem richtigen Teil der ursprünglichen Nachricht übereinstimmt, weiß der Client, dass der Server die ursprüngliche Nachricht mit dem gemeinsamen geheimen Sitzungsschlüssel entschlüsseln konnte und einen Teil dieser Nachricht mit demselben gemeinsamen geheimen [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly)erneut verschlüsseln konnte.

 

 
