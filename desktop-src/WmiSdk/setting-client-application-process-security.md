---
description: Clientanwendungen, die WMI-Schnittstellen aufrufen, können die Sicherheitsebenen ihrer Prozesse steuern.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Festlegen der Clientanwendungsprozesssicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739470"
---
# <a name="setting-client-application-process-security"></a>Festlegen der Clientanwendungsprozesssicherheit

Clientanwendungen, die WMI-Schnittstellen aufrufen, können die Sicherheitsebenen ihrer Prozesse steuern. Alle WMI-Anwendungen greifen über COM auf WMI zu, und Sie können die COM-Funktion [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um die Sicherheit für Ihre Prozesse festzulegen. Anwendungen, die Asynchrone Aufrufe an WMI vornehmen, und Anwendungen, die sich als Ereignisverbraucher registrieren, legen Sicherheitsstufen für den Aufruf von WMI fest.

Wenn Sie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht explizit aufrufen, ruft COM sie implizit mit Werten aus der Registrierung auf. Die Registrierungswerte verfügen jedoch möglicherweise über niedrigere Einstellungen für Identitätswechsel und Authentifizierung, die nicht die für WMI erforderliche Sicherheit bieten. Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit C++](setting-the-default-process-security-level-using-c-.md).

Der asynchrone Zugriff auf WMI wird nicht empfohlen. Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke bereitzustellen. Dies stellt Sicherheitsrisiken für Ihre Skripts und Anwendungen dar. Um die Risiken zu vermeiden, verwenden Sie semisynchrone oder synchrone Kommunikation, oder führen Sie in Ihrer Clientanwendung ordnungsgemäße Zugriffsüberprüfungen durch. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Aufrufe von WMI-Proxys ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**IEnumWbemClassObject,**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)oder [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) verwenden einen Out-of-Process-Zeiger. Weitere Informationen zu den Standardwerten und Empfehlungen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere Proxys.](setting-the-security-on-iwbemservices-and-other-proxies.md)

Im folgenden Verfahren werden die Schritte beschrieben, die Sie ausführen müssen, um die Sicherheit für WMI in Ihrem Anwendungsprozess festzulegen.

**So legen Sie die Sicherheit für WMI in Ihrem Anwendungsprozess fest**

1.  Bestimmen Sie die Sicherheitsstufen, die für die Windows Betriebssysteme erforderlich sind, unter denen Ihre Clientanwendung ausgeführt wird.
2.  Rufen Sie die COM [**CoInitializeSecurity-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) auf, um die Standardsicherheit für den Prozess festzulegen, in dem die Clientanwendung ausgeführt wird. Dadurch wird deklariert, wie viel Sicherheit andere Anwendungen für den Zugriff auf den Prozess benötigen, in dem Ihre Anwendung ausgeführt wird.
3.  Wenn Sie die Sicherheit für einen einzelnen Proxy ändern müssen, z. B. bei einem anderen Aufruf von [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)rufen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)auf.
4.  Wenn Sie Remotehardware oder ein Systemobjekt steuern müssen, das mehr Berechtigungen erfordert, verwenden Sie die [**Funktion AdjustTokenPrivileges,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) um die erforderlichen Berechtigungen zu aktivieren. Beachten Sie, dass Sie keine Berechtigung aktivieren können, die dem Prozess noch nicht zugewiesen wurde. Weitere Informationen finden Sie unter [Überprüfen des Zugriffs auf private Objekte.](/windows/desktop/SecAuthZ/checking-access-to-private-objects)

Weitere Informationen zum Festlegen der Standardprozesssicherheitsstufe finden Sie unter [Setting the Default Process Security Level Using C++ (Festlegen der Standardprozesssicherheitsstufe mit C++)](setting-the-default-process-security-level-using-c-.md) und Setting the Default Process Security Level Using [VBScript (Festlegen der Standardprozesssicherheitsstufe mit VBScript).](setting-the-default-process-security-level-using-vbscript.md)

 

 
