---
description: Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remote System abruft, stellt WMI Ihre Anmelde Informationen für den Anbieter der Daten auf dem Remote System bereit.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegierung mit WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393866"
---
# <a name="delegating-with-wmi"></a>Delegierung mit WMI

Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remote System abruft, stellt WMI Ihre Anmelde Informationen für den Anbieter der Daten auf dem Remote System bereit. Dies erfordert nur eine Identitätswechsel **Ebene des Identitäts** Wechsels, da nur ein Netzwerkhop erforderlich ist. Wenn das Skript jedoch eine Verbindung mit WMI auf dem Remote System herstellt und versucht, eine Protokolldatei auf einem zusätzlichen Remote System zu öffnen, schlägt das Skript fehl, es sei denn, die Identitätswechsel **Ebene ist "** Delegat".  Die Identitätswechsel Ebene des Delegaten ist für jeden Vorgang erforderlich, der mehr als einen Netzwerkhop umfasst. Weitere Informationen zur DCOM-Sicherheit in WMI finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md). Weitere Informationen zu einer Verbindung mit einem Netzwerk Hop zwischen zwei Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

**So verwenden Sie die Delegierung für die Verbindung mit einem Computer über einen anderen Computer**

1.  Aktivieren Sie die Delegierung in Active Directory (**Active Directory Benutzer und Computer** in der **System Steuerungs** **Verwaltungsaufgabe**) auf dem Domänen Controller. Das Konto auf dem Remote System muss **für die Delegierung als vertrauenswürdig** gekennzeichnet sein, und das Konto auf dem lokalen System darf nicht als Konto vertraulich gekennzeichnet **und kann nicht delegiert** werden. das lokale System, das Remote System und der Domänen Controller müssen Mitglieder derselben Domäne oder in vertrauenswürdigen Domänen sein.

    **Hinweis**  Die Verwendung der Delegierung stellt ein Sicherheitsrisiko dar, da Prozesse außerhalb ihrer direkten Kontrolle die Möglichkeit zur Verwendung Ihrer Anmelde Informationen bieten.

2.  Ändern Sie den Code wie folgt, um anzugeben, dass Sie die Delegierung verwenden möchten.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell
    </dt> <dd>

    Legen Sie den Parameter-Identitäts **Wechsel für das** WMI *-* Cmdlet auf Delegat fest.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript
    </dt> <dd>

    Legen Sie den Parameter "Identitätswechsel *Ebene* " auf "Delegat" fest, indem Sie in der [Monikerzeichenfolge](constructing-a-moniker-string.md) auf " [Swap-Server](swbemlocator-connectserver.md) **" oder "** Delegat" **delegieren** . Sie können auch den Identitätswechsel in einem " [**Swap Security**](swbemsecurity.md)"-Objekt festlegen.

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Legen Sie im Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)den Parameter für die Identitätswechsel Ebene auf den **RPC-C- \_ \_ IMP- \_ Ebenen \_** -Delegaten fest. Weitere Informationen dazu, wann diese Aufrufe durchführen werden sollten, finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).

    Um die Client Identität an Remote-com-Server in C++ zu übergeben, legen Sie das Cloaking im Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest. Weitere Informationen finden Sie unter [Cloaking](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt eine Monikerzeichenfolge, die den Identitätswechsel zum Delegaten **festlegt.** Beachten Sie, dass die Autorität auf Kerberos festgelegt werden muss.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



Im folgenden Codebeispiel wird veranschaulicht, wie der Identitätswechsel **mithilfe von "** [**Swap-Server**](swbemlocator-connectserver.md)" (ein Wert von 4) festgelegt wird.


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Erstellen von Prozessen per Remote Verbindung mit WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
