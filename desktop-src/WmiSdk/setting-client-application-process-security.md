---
description: Client Anwendungen, die WMI-Schnittstellen aufzurufen, können die Sicherheitsstufen ihrer Prozesse steuern.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Festlegen der Prozesssicherheit für Client Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bfa0a42390ffa433cff01300b0976d40553665c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216889"
---
# <a name="setting-client-application-process-security"></a>Festlegen der Prozesssicherheit für Client Anwendungen

Client Anwendungen, die WMI-Schnittstellen aufzurufen, können die Sicherheitsstufen ihrer Prozesse steuern. Alle WMI-Anwendungen greifen über com auf WMI zu, und Sie können die com-Funktion [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um die Sicherheit für Ihre Prozesse festzulegen. Anwendungen, die asynchrone Aufrufe von WMI und Anwendungen ausführen, die als Ereignisconsumer registriert werden, legen Sicherheitsebenen für den WMI-Aufruf fest.

Wenn Sie keinen expliziten Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)durchführen, ruft com ihn implizit mit Werten aus der Registrierung auf. Die Registrierungs Werte haben jedoch möglicherweise niedrigere Einstellungen für Identitätswechsel und Authentifizierung, die nicht die für WMI erforderliche Sicherheit bereitstellen. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).

Der asynchrone Zugriff auf WMI wird nicht empfohlen. Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation, oder führen Sie in der Client Anwendung ordnungsgemäße Zugriffs Überprüfungen durch. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Aufrufe von WMI-Proxys ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)oder [**iwbemaktusher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) verwenden einen Out-of-Process-Zeiger. Weitere Informationen zu den Standardeinstellungen und Empfehlungen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.

Im folgenden Verfahren werden die Schritte beschrieben, die Sie ausführen müssen, um die Sicherheit für WMI auf dem Anwendungsprozess festzulegen.

**So legen Sie die Sicherheit für WMI für den Anwendungsprozess fest**

1.  Bestimmen Sie die Sicherheitsstufen, die für die Windows-Betriebssysteme erforderlich sind, auf denen die Client Anwendung ausgeführt wird.
2.  Ruft die com- [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion auf, um die Standard Sicherheit für den Prozess festzulegen, in dem die Client Anwendung ausgeführt wird. Dadurch wird angegeben, wie viel Sicherheit andere Anwendungen benötigen, um auf den Prozess zuzugreifen, in dem Ihre Anwendung ausgeführt wird.
3.  Wenn Sie die Sicherheit eines einzelnen Proxys ändern müssen, z. b. bei einem anderen [**callbemservices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)-Befehl, aufrufen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Wenn Sie Remote Hardware oder ein Systemobjekt steuern müssen, das mehr Berechtigungen erfordert, verwenden Sie [**die Funktion "**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) Funktion", um die erforderlichen Berechtigungen zu aktivieren. Beachten Sie, dass Sie keine Berechtigung aktivieren können, die dem Prozess nicht bereits zugewiesen wurde. Weitere Informationen finden Sie unter über [prüfen des Zugriffs auf private Objekte](/windows/desktop/SecAuthZ/checking-access-to-private-objects).

Weitere Informationen zum Festlegen der standardmäßigen Prozess Sicherheitsstufe finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md) und [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
