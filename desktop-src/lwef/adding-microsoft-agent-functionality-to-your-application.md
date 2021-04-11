---
title: Hinzufügen von Microsoft-Agent-Funktionen zu Ihrer Anwendung
description: Hinzufügen von Microsoft-Agent-Funktionen zu Ihrer Anwendung
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314835"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Hinzufügen von Microsoft-Agent-Funktionen zu Ihrer Anwendung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Um auf die Server Schnittstellen von Microsoft Agent zuzugreifen, muss der-Agent bereits auf dem Zielsystem installiert sein. Die Installation außer der selbst Installationsdatei des Agents, wie z. b. der Versuch, agentkomponentendateien zu kopieren und zu registrieren, wird nicht unterstützt. Dadurch wird eine konsistente und umfassende Installation sichergestellt. Beachten Sie, dass die selbst Installationsdatei des Microsoft-Agents nicht unter Microsoft Windows 2000 und höheren Betriebssystemen installiert werden kann, da diese Versionen des Betriebssystems bereits eine eigene Agent-Version enthalten.

Um den-Agent erfolgreich auf einem Zielsystem mit einem früheren Microsoft Windows-Betriebssystem zu installieren, müssen Sie auch sicherstellen, dass das Zielsystem über eine aktuelle Version der Microsoft Visual C++ Runtime (Msvcrt.dll), des Microsoft-Registrierungs Tools (Regsvr32.dll) und der Microsoft com-DLLs verfügt. Die einfachste Möglichkeit, um sicherzustellen, dass die erforderlichen Komponenten auf dem Zielsystem installiert sind, besteht darin, dass Microsoft Internet Explorer 3,02 oder höher installiert ist. Alternativ können Sie die ersten beiden Komponenten installieren, die als Teil Microsoft Visual C++ verfügbar sind. Die erforderlichen COM-DLLs können als Teil des Microsoft DCOM-Updates installiert werden, das auf der Microsoft-Website verfügbar ist. Weitere Informationen und Lizenzierungsinformationen zu diesen Komponenten finden Sie auf der Microsoft-Website.

Die Sprachkomponenten des Agents können auf die gleiche Weise installiert werden. Auf ähnliche Weise können Sie diese Technik verwenden, um das ACS-Format der Microsoft-Zeichen zu installieren, die für die Verteilung auf der Microsoft Agent-Website verfügbar sind. Die Zeichen Dateien werden automatisch im Unterverzeichnis Microsoft-Agent- \\ chars installiert.

Da die Komponenten des Microsoft-Agents als Betriebssystemkomponenten entworfen wurden, ist der-Agent möglicherweise nicht deinstalliert. Ebenso, wo der-Agent bereits als Teil des Windows-Betriebssystems installiert ist, kann die CAB-Datei des Agents möglicherweise nicht installiert werden.

Wenn die Schnittstellen des Agents aufgerufen wurden, erstellen Sie eine Instanz des Servers, und fordern Sie einen Zeiger auf eine bestimmte Schnittstelle an, die der Server unter Verwendung der com-Standard Konvention unterstützt. Insbesondere die com-Bibliothek stellt eine API-Funktion, [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), bereit, die eine Instanz des-Objekts erstellt und einen Zeiger auf die angeforderte Schnittstelle des-Objekts zurückgibt. Fordern Sie einen Zeiger auf die [**iagent**](iagent.md) -oder [**iagentex**](iagentex.md) -Schnittstelle in Ihrem **copurateinstance** -Befehl oder in einem nachfolgenden Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))an.

Der folgende Code veranschaulicht dies in C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Wenn der Microsoft-Agent-Server ausgeführt wird, stellt diese Funktion eine Verbindung mit dem Server her. Andernfalls wird der Server gestartet.

Beachten Sie, dass die Microsoft-Agent-Server Schnittstellen häufig Erweiterte Schnittstellen enthalten, die das Suffix "ex" enthalten. Diese Schnittstellen werden von abgeleitet und enthalten daher sämtliche Funktionen von, ihre nicht-Ex-Entsprechungen. Wenn Sie eine der erweiterten Features verwenden möchten, verwenden Sie die Ex-Schnittstellen.

Funktionen, die Zeiger auf bstrins verwenden, belegen mithilfe von [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)Arbeitsspeicher. Es liegt in der Verantwortung des Aufrufers, diesen Arbeitsspeicher mit [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)freizugeben.

 

 