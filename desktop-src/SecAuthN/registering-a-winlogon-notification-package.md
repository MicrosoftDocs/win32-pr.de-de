---
description: Informationen zu Winlogon-Benachrichtigungs Paketen werden in der Registrierung gespeichert. Registrierungseinträge geben den Namen des Benachrichtigungs Pakets, den Namen der dll, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse verarbeiten.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrieren eines Winlogon-Benachrichtigungs Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215880"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrieren eines Winlogon-Benachrichtigungs Pakets

Informationen zu [*Winlogon*](../secgloss/w-gly.md) -Benachrichtigungs Paketen werden in der Registrierung gespeichert. Registrierungseinträge geben den Namen des Benachrichtigungs Pakets, den Namen der dll, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse verarbeiten.

Wenn Winlogon gestartet wird, wird die Registrierung überprüft und alle registrierten Benachrichtigungs Pakete geladen. Wenn ein Ereignis auftritt, ruft Winlogon die festgelegte Ereignishandlerfunktion für jedes Paket auf. Mehrere Ereignis Benachrichtigungs Pakete können auf einem System registriert werden.

Erstellen Sie zum Registrieren des Benachrichtigungs Pakets einen Registrierungsschlüssel mit dem Namen **Benachrichtigen** als Unterschlüssel des folgenden Registrierungsschlüssels, und fügen Sie die in den [Registrierungs Einträgen](registry-entries.md)beschriebenen Werte hinzu.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
