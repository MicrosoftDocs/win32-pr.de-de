---
description: Eine Serveranwendung kann die Funktion "-Funktion" aufrufen, um einen neuen Prozess zu erstellen, der im Sicherheitskontext eines Clients ausgeführt wird.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Prozesse im Client Sicherheitskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372877"
---
# <a name="processes-in-the-client-security-context"></a>Prozesse im Client Sicherheitskontext

Eine Serveranwendung [**kann die Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) "-Funktion" aufrufen, um einen neuen Prozess zu erstellen, der im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)eines Clients ausgeführt wird. Wenn der Aufruf mit dem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)eines Clients erfolgt, benötigt " **fiateprocessasuser** " den Namen "SE zuordnername" \_ \_ und "SE \_ Erhöhung \_ Quota Name" \_ , die von Windows-Diensten, die im [LocalSystem-Konto](/windows/desktop/Services/localsystem-account)ausgeführt werden, gehalten werden.

Die Funktion " [**fiateprocessasuser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " erfordert auch ein [*Primäres Zugriffs Token*](/windows/desktop/SecGloss/p-gly). Ein Server kann ein primäres Zugriffs Token für einen Client abrufen, indem er entweder [eine Anmelde Sitzung](client-logon-sessions.md) für den Client startet oder die Identität [des Clients](client-impersonation.md) annimmt und das Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly)duplizieren.

In den folgenden Verfahren werden zwei Möglichkeiten zum Erstellen eines Client Prozesses beschrieben.

**So erstellen Sie einen Client Prozess durch Anmelden beim Client**

1.  Melden Sie den Client mithilfe der Anmelde Informationen des Clients bei einem [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera)- [*Anmelde*](/windows/desktop/SecGloss/c-gly) Name auf dem lokalen Computer an. **LogonUser** erstellt ein primäres Token für die [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly)des Clients.
2.  Wenn der Server den Sicherheitskontext des Clients verwenden muss, erhalten Sie Zugriff auf die ausführbare Datei für den Client [*Prozess*](/windows/desktop/SecGloss/p-gly) , indem Sie das primäre Token in einem Aufrufen der Identität [**ateloggedonuser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) -Funktion verwenden.
3.  Erstellen Sie einen Prozess im Sicherheitskontext des [**Clients, indem Sie das**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)primäre Token in einem aufzurufenden aufzurufen.

> [!Note]  
> Ein mit der folgenden Technik erstellter Prozess kann möglicherweise nicht auf Netzwerkressourcen zugreifen, es sei denn, er verfügt über die [*Anmelde*](/windows/desktop/SecGloss/c-gly)Informationen des Clients.

 

**So erstellen Sie einen Client Prozess durch annehmen der Identität des Clients**

1.  Starten Sie den Identitätswechsel, indem Sie eine Identitätswechsel Funktion verwenden, z. b. "Identität- [**amedpipeclient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)".
2.  Zum Abrufen eines Identitätswechsel Tokens, das den Sicherheitskontext des Clients enthält, können Sie die [**openthread Token**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) -Funktion abrufen.
3.  Aufrufen der [**Dupli-etokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) -Funktion, um das Identitätswechsel Token in ein primäres Token zu konvertieren.
4.  Verwenden Sie das primäre Token in einem Aufrufen der [**Funktion "**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ", um einen Prozess im Sicherheitskontext des Clients zu erstellen.

Standard [**mäßig erstellt der**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Client [*Prozess*](/windows/desktop/SecGloss/p-gly) in einer nicht interaktiven Fenster Station und einem Desktop. Um einen interaktiven Prozess zu erstellen, muss der Server zunächst die freigegebenen [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/d-gly) (DACLs) der interaktiven Fenster Station und des Desktops festlegen, um sicherzustellen, dass dem Client der Zugriff gewährt wird. Die bevorzugte Vorgehensweise besteht darin, den Client zu protokollieren, [die Sicherheits-ID (SID) der Anmelde Sitzung des Clients zu erhalten](/previous-versions//aa446670(v=vs.85))und diese SID dann in Zugriffs zulässigen ACEs sowohl auf der interaktiven Fenster Station als auch auf dem Desktop zu verwenden. Der Server kann dann " **kreateprocessasuser**" aufrufen, wobei die interaktive Fenster Station und der Desktop WinSta0 Standard angegeben werden \\ . Ein Beispiel für diese Prozedur finden Sie unter [Starten eines interaktiven Client Prozesses in C++](/previous-versions//aa379608(v=vs.85)).

 

 
