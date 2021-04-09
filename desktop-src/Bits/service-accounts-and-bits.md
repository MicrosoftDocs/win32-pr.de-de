---
title: Dienst Konten und Bits
description: Sie können Bits verwenden, um Dateien von einem Dienst zu übertragen. Der Dienst muss das Systemkonto "LocalSystem", "LocalService" oder "Network Service" verwenden. Diese Konten sind immer angemeldet. aus diesem Grund werden Aufträge, die von einem Dienst übermittelt werden, immer ausgeführt.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- Dienst Konten Bits
- Übertragen von Auftrags Bits, Besitz, Dienst Konto
- Proxy Bits, Dienst Konten
- Anmelde Informationen zum Übertragen von Auftrags Bits
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 475a623e6b105d3ef2bdc6586db613c010fe8923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101807"
---
# <a name="service-accounts-and-bits"></a>Dienst Konten und Bits

Sie können Bits verwenden, um Dateien von einem Dienst zu übertragen. Der Dienst muss das Systemkonto "LocalSystem", "LocalService" oder "Network Service" verwenden. Diese Konten sind immer angemeldet. aus diesem Grund werden Aufträge, die von einem Dienst übermittelt werden, immer ausgeführt.

Wenn ein Dienst, der unter einem Systemkonto ausgeführt wird, die Identität des Benutzers annimmt, bevor Bits aufgerufen wird, antwortet Bits wie für ein beliebiges Benutzerkonto (z. b. muss der Benutzer auf dem Computer angemeldet sein, damit die Übertragung erfolgt). Der Dienst sollte auch dynamische Cloaking mit den Bits-Schnittstellen Zeigern verwenden, wenn die Identität des Benutzers angenommen wird. Das Cloaking ist nicht vererbt. Daher müssen Sie die [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -Funktion für jeden Schnittstellen Zeiger aufrufen, den Sie von Bits empfangen (z. b. durch den Aufruf der [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode zurückgegebenen Auftrags Zeiger); Es genügt nicht, das Cloaking für den Manager-Schnittstellen Zeiger festzulegen. Sie können auch die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion für den Prozess aufrufen, anstatt die **CoSetProxyBlanket** -Funktion für jeden Schnittstellen Zeiger aufzurufen.

Wenn der Dienst die Identität des Benutzers jedoch nicht annimmt, gelten die folgenden Verhaltensweisen:

- Die vom Dienst Konto erstellten Aufträge befinden sich im Besitz dieses Kontos. Da Systemkonten immer angemeldet sind, überträgt Bits die Dateien so lange, wie der Computer ausgeführt wird und eine Netzwerkverbindung besteht.
- System Konten sollten keine zugeordneten Netzwerklaufwerks Buchstaben verwenden, da die Laufwerk Buchstaben für eine Sitzung spezifisch sind und die Zuordnung nach einem Neustart des Computers möglicherweise verloren geht.
- Wenn kein Hilfstoken [vorhanden ist,](helper-tokens-for-bits-transfer-jobs.md)verwendet die Netzwerk Authentifizierung Computer Anmelde Informationen für die Konten "LocalSystem" und "NetworkService" und anonyme Anmelde Informationen für das Konto "LocalService". Bits gibt "Zugriff verweigert" zurück, wenn die Zugriffs Steuerungs Liste (Access Control List, ACL) für die Quelldatei den Zugriff auf ein Benutzerkonto einschränkt.
- Ausführliche Informationen zur Funktionsweise der Authentifizierung bei vorhanden sein eines [Hilfsobjekts](helper-tokens-for-bits-transfer-jobs.md)finden Sie unter [Authentifizierung](authentication.md).
- Microsoft Internet Explorer-Proxy Einstellungen werden pro Benutzer gespeichert und sind nicht für Systemkonten festgelegt. Sie sollten ein Hilfsobjekt für ihre Bits-Aufträge konfigurieren oder die korrekten Proxy Einstellungen explizit festlegen, indem Sie [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der **außer Kraft setzung der BG- \_ Auftrags \_ Proxy \_ Verwendung \_** aufrufen. Alternativ können Sie die **/util/SetIEProxy** -Schalter von BitsAdmin.exe verwenden, um Internet Explorer-Proxy Einstellungen für das Systemkonto "LocalSystem", "LocalService" oder "Network Service" festzulegen. Weitere Informationen finden Sie unter [bitadmin-Tool](bitsadmin-tool.md).

Beachten Sie, dass Bits die Proxy Einstellungen nicht erkennt, die mithilfe der Proxycfg.exe Datei festgelegt werden.