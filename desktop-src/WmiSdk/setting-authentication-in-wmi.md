---
description: Wenn Aufrufe außerhalb des aufrufenden Prozesses oder eines WMI-Remote Dienstanbieter durchführen, verwendet WMI die verteilte Version des Component Object Model (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Festlegen der Authentifizierung in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216890"
---
# <a name="setting-authentication-in-wmi"></a>Festlegen der Authentifizierung in WMI

Wenn Aufrufe außerhalb des aufrufenden Prozesses oder eines WMI-Remote Dienstanbieter durchführen, verwendet WMI die verteilte Version des Component Object Model (DCOM). Out-of-Process-und Remote Aufrufe werden über Proxys durchgeführt, für die eine Authentifizierung der Anmelde Informationen des aufrufenden Prozesses erforderlich ist.

Beim Herstellen einer Verbindung mit einem Computer und einem WMI-Namespace legen Sie die Authentifizierungs Ebene fest. Um eine Verbindung mit WMI herzustellen, nennen Sie [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) in C++. Bei der Skripterstellung oder Visual Basic stellen Sie eine Verbindung mit WMI mithilfe von "WS-Locator. ConnectServer" oder der [Monikerzeichenfolge](constructing-a-moniker-string.md) her. DCOM-Sicherheit und WMI erfordern bei der Verbindungs Herstellung zwischen Computern bestimmte Authentifizierungs Ebenen. Die erforderliche Ebene unterscheidet sich je nach Betriebssystem, das Sie verbinden. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

WMI wird normalerweise auf einem gemeinsamen Dienst Host ausgeführt und verwendet dieselbe Authentifizierung wie andere Prozesse auf dem Host. Um den WMI-Prozess mit einer anderen Authentifizierungs Stufe auszuführen, führen Sie WMI mit dem [**WinMgmt**](winmgmt.md) -Befehl mit dem Schalter **/standalonehost** aus, und legen Sie die Authentifizierungs Ebene für WMI in der Regel fest. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

Weitere Informationen und Codebeispiele zum Festlegen der Authentifizierung für WMI-Verbindungen finden Sie unter [Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript](setting-the-authentication-service-using-vbscript.md) und [Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md). Diese Themen enthalten auch Tabellen, in denen die Authentifizierungs Konstanten für C++ und Skripterstellung aufgeführt sind.

## <a name="using-proxies-in-wmi"></a>Verwenden von Proxys in WMI

Um die Authentifizierung für einen Proxy festzulegen, müssen Sie die [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -Funktion aufrufen. Weitere Informationen und ein Codebeispiel finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.

Die folgende [com-API für WMI](com-api-for-wmi.md) -Objekte verwendet Proxys direkt in C++ oder c#, um den Prozess oder einen Remote-WMI-Dienst aufzurufen:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**Ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**Iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**Iwbemfreshsher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Die Skript Objekte, wie z. b. " [**errbefubject**](swbemobject.md)", " [**errbemservices**](swbemservices.md)" und " [**errbemfreshsher**](swbemrefresher.md) ", verwenden keine Proxys. Stattdessen stellen die Skript Objekte einen Wrapper oder eine Ebene dar, die die oben aufgeführten [com-API für WMI](com-api-for-wmi.md) -Objekte aufruft. Weitere Informationen und ein Codebeispiel zum Festlegen der Authentifizierung bei der Skripterstellung finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
