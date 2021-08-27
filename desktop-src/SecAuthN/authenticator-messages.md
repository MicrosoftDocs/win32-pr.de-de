---
description: In einem einfachen Protokoll mit Authentifizierung mit geheimen Schlüsseln stellt ein Client eine Authentifikatornachricht in Form einer Information dar, die im Sitzungsschlüssel verschlüsselt ist.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Authenticator Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc21cd87fbf1b725f276f138bcd0bd513658428ddd1296c4016542953bd8b86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035460"
---
# <a name="authenticator-messages"></a>Authenticator Nachrichten

In einem einfachen Protokoll mit Authentifizierung mit geheimen Schlüsseln stellt ein Client eine Authentifikatornachricht in Form einer Information dar, die im [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly)verschlüsselt ist. Die Informationen in der Authentifikatornachricht müssen bei jeder Ausführung des Authentifizierungsprotokolls unterschiedlich sein. Andernfalls kann eine verschlüsselte Authentifikatornachricht von einer nicht autorisierten Entität wiederverwendet werden.

Beim Empfang der Authentifikatornachricht entschlüsselt der Server sie und kann anhand des Inhalts der entschlüsselten Nachricht erkennen, ob die Entschlüsselung erfolgreich war. Wenn die entschlüsselte Nachricht nicht unbändig ist, weiß der Server, dass der Client, der die Authentifikatornachricht darstellt, den richtigen Schlüssel zum Verschlüsseln der Nachricht verwendet hat. Nur zwei Entitäten haben Zugriff auf den [*Sitzungsschlüssel.*](/windows/desktop/SecGloss/s-gly) Wenn der Server einer dieser Entitäten ist, muss der Client, der die Authentifikatornachricht verschlüsselt hat, der andere sein.

Für die gegenseitige Authentifizierung wird ein ähnliches Protokoll ausgeführt. Der Server extrahiert einen Teil der Informationen aus der entschlüsselten ursprünglichen Authentifikatornachricht, verschlüsselt sie mit dem freigegebenen Sitzungsschlüssel und sendet die verschlüsselte Nachricht an den Client. Der Client entschlüsselt die Nachricht und vergleicht das Ergebnis mit dem Original. Wenn die entschlüsselte Nachricht mit dem richtigen Teil der ursprünglichen Nachricht übereinstimmt, weiß der Client, dass der Server die ursprüngliche Nachricht mit dem gemeinsam verwendeten geheimen Sitzungsschlüssel entschlüsseln und einen Teil dieser Nachricht mit demselben gemeinsam verwendeten geheimen [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly)erneut verschlüsseln konnte.

 

 
