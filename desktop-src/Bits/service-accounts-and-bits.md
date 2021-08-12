---
title: Dienstkonten und BITS
description: Sie können BITS verwenden, um Dateien von einem Dienst zu übertragen. Der Dienst muss das Systemkonto LocalSystem, LocalService oder NetworkService verwenden. Diese Konten sind immer angemeldet. Daher werden aufträge, die von einem Dienst mit diesen Konten übermittelt werden, immer ausgeführt.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- Dienstkonten BITS
- Übertragungsauftrag BITS , Besitz, Dienstkonto
- Proxy BITS , Dienstkonten
- Anmeldeinformationen zum Übertragen von Auftrags-BITS
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679902"
---
# <a name="service-accounts-and-bits"></a>Dienstkonten und BITS

Sie können BITS verwenden, um Dateien von einem Dienst zu übertragen. Der Dienst muss das Systemkonto LocalSystem, LocalService oder NetworkService verwenden. Diese Konten sind immer angemeldet. Daher werden aufträge, die von einem Dienst mit diesen Konten übermittelt werden, immer ausgeführt.

Wenn ein Dienst, der unter einem Systemkonto ausgeführt wird, die Identität des Benutzers vor dem Aufrufen von BITS antspricht, antwortet BITS wie bei jedem Benutzerkonto (z. B. muss der Benutzer beim Computer angemeldet sein, damit die Übertragung erfolgt). Der Dienst sollte beim Identitätswechsel des Benutzers auch dynamisches Cloaking mit den BITS-Schnittstellenzedern verwenden. Cloaking wird nicht geerbt, daher müssen Sie die [**CoSetProxyBlanket-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) für jeden Schnittstellenzeiger aufrufen, den Sie von BITS erhalten (z. B. den Auftragszeiger, der beim Aufrufen der [**IBackgroundCopyManager::CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) zurückgegeben wurde). es reicht nicht aus, die Verhenkung für den Manager-Schnittstellenzeiger zu setzen. Sie können auch die [**CoInitializeSecurity-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) für den Prozess aufrufen, anstatt die **CoSetProxyBlanket-Funktion** für jeden Schnittstellenzeiger auf aufruft.

Wenn der Dienst jedoch nicht die Identität des Benutzers antspricht, gelten die folgenden Verhaltensweisen:

- Aufträge, die vom Dienstkonto erstellt werden, befinden sich im Besitz dieses Kontos. Da Systemkonten immer angemeldet sind, überträgt BITS die Dateien, solange der Computer ausgeführt wird und eine Netzwerkverbindung besteht.
- Systemkonten sollten keine zugeordneten Netzlaufwerkbuchstaben verwenden, da die Laufwerkbuchstaben für eine Sitzung spezifisch sind und die Zuordnung nach einem Computerneustart möglicherweise verloren geht.
- Ohne Hilfstoken [](helper-tokens-for-bits-transfer-jobs.md)verwendet die Netzwerkauthentifizierung Computeranmeldeinformationen für LocalSystem- und NetworkService-Konten und anonyme Anmeldeinformationen für das LocalService-Konto. BITS gibt "Zugriff verweigert" zurück, wenn die Zugriffssteuerungsliste (Access Control List, ACL) für die Quelldatei den Zugriff auf ein Benutzerkonto einschränkt.
- Weitere Informationen zur Funktionsweise der Authentifizierung bei Vorhandensein eines [Hilfstokens finden](helper-tokens-for-bits-transfer-jobs.md)Sie unter [Authentifizierung](authentication.md).
- Microsoft Internet Explorer Proxyeinstellungen werden pro Benutzer gespeichert und nicht für Systemkonten festgelegt. Erwägen Sie die Konfiguration eines Hilfstokens für Ihre BITS-Aufträge, oder legen Sie explizit die richtigen Proxyeinstellungen fest, indem [**Sie IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **BG JOB PROXY USAGE OVERRIDE \_ \_ \_ \_ aufrufen.** Alternativ können Sie die Schalter **/Util /SetIEProxy** von BitsAdmin.exe verwenden, um Internet Explorer-Proxyeinstellungen für das Systemkonto LocalSystem, LocalService oder NetworkService festlegen. Weitere Informationen finden Sie unter [BitsAdmin Tool](bitsadmin-tool.md).

Beachten Sie, dass BITS die Proxyeinstellungen nicht erkennt, die mithilfe der Proxycfg.exe werden.