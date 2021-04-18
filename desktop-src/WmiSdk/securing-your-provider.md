---
description: Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel übernimmt und sicherstellen, dass die Benutzer auf die Daten zugreifen können.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sichern Ihres Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347068"
---
# <a name="securing-your-provider"></a>Sichern Ihres Anbieters

Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel übernimmt und sicherstellen, dass die Benutzer auf die Daten zugreifen können. Sie können die Daten im Anbieter Namespace sichern, indem Sie die Verschlüsselung von Daten vor dem Senden über ein Netzwerk vorschreiben. Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Wenn ein Benutzer über **vollständigen \_ Schreib** Zugriff in einem Namespace verfügt, kann der Benutzer Namespace übergreifende Abonnements für Daten in einem Namespace erstellen, in dem der Benutzer eingeschränkt ist. Da ein Anbieter in beliebige Namespaces geladen und in einem beliebigen Sicherheitskontext ausgeführt werden kann, sollte der Anbieter seine eigenen Zugriffs Überprüfungen durchführen, um sicherzustellen, dass nur autorisierte Benutzer Zugriff auf Daten haben oder Methoden ausführen. Weitere Informationen finden Sie unter [Durchführen von Zugriffs Überprüfungen](performing-access-checks.md).

In den folgenden Themen wird die Anbieter Sicherheit erörtert:

-   [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md)
-   [Ausführen von Zugriffs Überprüfungen](performing-access-checks.md)
-   [Registrierungsschlüssel zum Steuern der Anbieter Sicherheit](registry-keys-for-controlling-provider-security-.md)
-   [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
-   [Annehmen der Identität eines Clients](impersonating-a-client.md)

In den folgenden Themen wird erläutert, wie Clients und Skripts mit der Anbieter Sicherheit interagieren:

-   [Festlegen der Authentifizierung in WMI](setting-authentication-in-wmi.md)
-   [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
