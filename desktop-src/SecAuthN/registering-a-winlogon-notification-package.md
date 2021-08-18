---
description: Informationen zu Winlogon-Benachrichtigungspaketen werden in der Registrierung gespeichert. Registrierungseinträge geben den Namen des Benachrichtigungspakets, den Namen der DLL, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse behandeln.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrieren eines Winlogon-Benachrichtigungspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa41948062458581d607b64432166b99ba4701865a3c7b593365c87342359ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919669"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrieren eines Winlogon-Benachrichtigungspakets

Informationen zu [*Winlogon-Benachrichtigungspaketen*](../secgloss/w-gly.md) werden in der Registrierung gespeichert. Registrierungseinträge geben den Namen des Benachrichtigungspakets, den Namen der DLL, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse behandeln.

Wenn winlogon gestartet wird, wird die Registrierung überprüft und alle registrierten Benachrichtigungspakete geladen. Wenn ein Ereignis auftritt, ruft Winlogon die designierte Ereignishandlerfunktion für jedes Paket auf. Mehrere Ereignisbenachrichtigungspakete können auf einem System registriert werden.

Um Ihr Benachrichtigungspaket zu registrieren, erstellen Sie einen Registrierungsschlüssel mit dem Namen **Notify** als Unterschlüssel des folgenden Registrierungsschlüssels, und fügen Sie die Werte hinzu, die unter [Registrierungseinträge ausführlich sind.](registry-entries.md)

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
