---
description: Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel behandelt, und sicherstellen, dass Benutzer auf Zugriffsrechte für Daten überprüft werden.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Schützen Ihres Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dec112c7e207a23d36700d8fb5de3b3964590b514f9cf5a6aa5fbc03243cf40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732840"
---
# <a name="securing-your-provider"></a>Schützen Ihres Anbieters

Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel behandelt, und sicherstellen, dass Benutzer auf Zugriffsrechte für Daten überprüft werden. Sie können die Daten in Ihrem Anbieternamespace schützen, indem Sie vor dem Senden über ein Netzwerk eine verschlüsselte Authentifizierung der Daten verlangen. Weitere Informationen finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

Wenn ein Benutzer in einem beliebigen Namespace **\_ über VOLLSTÄNDIGEN SCHREIBzugriff** verfügt, kann der Benutzer namespaceübergreifende Abonnements für Daten in einem Namespace erstellen, in dem der Benutzer eingeschränkt ist. Da ein Anbieter in einen beliebigen Namespace geladen und in einem beliebigen Sicherheitskontext ausgeführt werden kann, sollte der Anbieter eigene Zugriffsüberprüfungen durchführen, um sicherzustellen, dass nur autorisierte Benutzer Zugriff auf Daten erhalten oder Methoden ausführen können. Weitere Informationen finden Sie unter [Ausführen von Zugriffsüberprüfungen.](performing-access-checks.md)

In den folgenden Themen wird die Anbietersicherheit behandelt:

-   [Anbieterhosting und -sicherheit](provider-hosting-and-security.md)
-   [Ausführen von Zugriffsüberprüfungen](performing-access-checks.md)
-   [Registrierungsschlüssel zum Steuern der Anbietersicherheit](registry-keys-for-controlling-provider-security-.md)
-   [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
-   [Identitätswechsel für einen Client](impersonating-a-client.md)

In den folgenden Themen wird die Interaktion von Clients und Skripts mit der Anbietersicherheit behandelt:

-   [Festlegen der Authentifizierung in WMI](setting-authentication-in-wmi.md)
-   [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Festlegen der Sicherheit des Clientanwendungsprozesses](setting-client-application-process-security.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
