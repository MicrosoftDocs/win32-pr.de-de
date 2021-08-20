---
description: Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remotesystem erhält, stellt WMI Ihre Anmeldeinformationen dem Anbieter der Daten auf dem Remotesystem zur Seite.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegieren mit WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca844363816e7800aa8b293b86b1b5fe14a7d145773d209da53ebaba4e119abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109154"
---
# <a name="delegating-with-wmi"></a>Delegieren mit WMI

Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remotesystem erhält, stellt WMI Ihre Anmeldeinformationen dem Anbieter der Daten auf dem Remotesystem zur Seite. Dies erfordert nur die Identitätswechselebene **Impersonate**, da nur ein Netzwerkhop erforderlich ist. Wenn das Skript jedoch eine Verbindung mit WMI auf dem Remotesystem herstellt und versucht, eine Protokolldatei auf einem zusätzlichen Remotesystem zu öffnen, schlägt das Skript fehl, es sei denn, die Identitätswechselebene ist **Delegat.** **Die Ebene** des Delegatwechsels ist für jeden Vorgang erforderlich, der mehrere Netzwerkhops umfasst. Weitere Informationen zur DCOM-Sicherheit in WMI finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md). Weitere Informationen zu einer Verbindung mit einem Netzwerkhop zwischen zwei Computern finden Sie unter Herstellen einer Verbindung mit [WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

**So verwenden Sie die Delegierung zum Herstellen einer Verbindung mit einem Computer über einen anderen Computer**

1.  Aktivieren Sie die Delegierung in Active Directory (**Active Directory-Benutzer und -Computer** in **Systemsteuerung** **Administrative Tasks**) auf dem Domänencontroller. Das Konto auf dem Remotesystem  muss für die Delegierung als Vertrauenswürdig gekennzeichnet sein, und das Konto auf dem lokalen System darf nicht als Konto ist vertraulich gekennzeichnet sein und **kann nicht delegiert werden.** das lokale System, das Remotesystem und der Domänencontroller müssen Mitglieder derselben Domäne oder in vertrauenswürdigen Domänen sein.

    **Hinweis:**  Die Verwendung der Delegierung stellt ein Sicherheitsrisiko dar, da Prozesse außerhalb Ihrer direkten Kontrolle die Möglichkeit erhalten, Ihre Anmeldeinformationen zu verwenden.

2.  Ändern Sie den Code wie folgt, um anzugeben, dass Sie die Delegierung verwenden möchten.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>Powershell
    </dt> <dd>

    Legen Sie *den Parameter -Impersonation* für das WMI-Cmdlet auf **Delegate fest.**

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>Vbscript
    </dt> <dd>

    Legen Sie den Parameter  *impersonationLevel* im Aufruf von [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) oder Delegate in der [Monikerzeichenfolge](constructing-a-moniker-string.md) auf **Delegate** fest. Sie können den Identitätswechsel auch in einem [**SWbemSecurity-Objekt**](swbemsecurity.md)festlegen.

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Legen Sie den Parameter für die Identitätswechselebene im Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)auf **RPC C IMP LEVEL \_ \_ \_ \_ DELEGATE** fest. Weitere Informationen zum Tätigen dieser Aufrufe finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

    Um die Clientidentität an COM-Remoteserver in C++ zu übergeben, legen Sie cloaking im Aufruf von [**CoSetProxyBlanket fest.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Weitere Informationen finden Sie unter [Cloaking](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt eine Monikerzeichenfolge, die den Identitätswechsel auf **Delegaten setzt.** Beachten Sie, dass die Autorität auf Kerberos festgelegt werden muss.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



Das folgende Codebeispiel zeigt, wie der Identitätswechsel mithilfe von [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md)auf **Delegate** (wert 4) festgelegt wird.


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

[Sichern einer WMI-Remoteverbindung](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Remote erstellen von Prozessen mit WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
