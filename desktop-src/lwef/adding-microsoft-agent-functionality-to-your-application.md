---
title: Hinzufügen von Microsoft Agent-Funktionen zu Ihrer Anwendung
description: Hinzufügen von Microsoft Agent-Funktionen zu Ihrer Anwendung
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf604a7e18d67865fb50981833ce808985e455118326c4f157258543e236dd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753129"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Hinzufügen von Microsoft Agent-Funktionen zu Ihrer Anwendung

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Für den Zugriff auf die Serverschnittstellen von Microsoft Agent muss der -Agent bereits auf dem Zielsystem installiert sein. Eine andere Installation als die Verwendung der selbstinstallierenden ausführbaren Datei des Agents, z. B. der Versuch, Agent-Komponentendateien zu kopieren und zu registrieren, wird nicht unterstützt. Dadurch wird eine konsistente und vollständige Installation sichergestellt. Beachten Sie, dass die Selbstinstallierungsdatei von Microsoft Agent nicht unter Microsoft Windows 2000 und höher installiert wird, da diese Versionen des Betriebssystems bereits eine eigene Version des -Agents enthalten.

Um den -Agent erfolgreich auf einem Zielsystem mit einem früheren Microsoft Windows-Betriebssystem zu installieren, müssen Sie auch sicherstellen, dass das Zielsystem über eine aktuelle Version der Microsoft Visual C++-Runtime (Msvcrt.dll), des Microsoft-Registrierungstool (Regsvr32.dll) und der Microsoft COM-DLL verfügt. Die einfachste Möglichkeit, sicherzustellen, dass sich die erforderlichen Komponenten auf dem Zielsystem befinden, besteht in der Installation von Microsoft Internet Explorer 3.02 oder höher. Alternativ können Sie die ersten beiden Komponenten installieren, die als Teil des Microsoft Visual C++. Die erforderlichen COM-DLLs können als Teil des Microsoft DCOM-Updates installiert werden, das auf der Microsoft-Website verfügbar ist. Weitere Informationen und Lizenzierungsinformationen für diese Komponenten finden Sie auf der Microsoft-Website.

Die Sprachkomponenten des Agents können auf die gleiche Weise installiert werden. Auf ähnliche Weise können Sie dieses Verfahren verwenden, um das ACS-Format der Microsoft-Zeichen zu installieren, die für die Verteilung über die Microsoft Agent-Website verfügbar sind. Die Zeichendateien werden automatisch im Microsoft Agent \\ Chars-Unterverzeichnis installiert.

Da die Komponenten von Microsoft Agent als Betriebssystemkomponenten entworfen wurden, wird der -Agent möglicherweise nicht deinstalliert. Wenn der -Agent bereits als Teil des betriebssystembasierten Windows installiert ist, wird die selbstinstallierte Agent-Schränkung möglicherweise nicht installiert.

Erstellen Sie nach der Installation zum Aufrufen der Schnittstellen des -Agents eine Instanz des Servers, und fordern Sie einen Zeiger auf eine bestimmte Schnittstelle an, die der Server unter Verwendung der COM-Standardkonvention unterstützt. Die COM-Bibliothek stellt insbesondere die API-Funktion [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)bereit, die eine Instanz des -Objekts erstellt und einen Zeiger auf die angeforderte Schnittstelle des Objekts zurückgibt. Fordern Sie einen Zeiger auf die [**IAgent-**](iagent.md) oder [**IAgentEx-Schnittstelle**](iagentex.md) in Ihrem **CoCreateInstance-Aufruf** oder in einem nachfolgenden Aufruf von [**QueryInterface an.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

Der folgende Code veranschaulicht dies in C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Wenn der Microsoft Agent-Server ausgeführt wird, stellt diese Funktion eine Verbindung mit dem Server herstellen. Andernfalls wird der Server gestartet.

Beachten Sie, dass die Microsoft Agent-Serverschnittstellen häufig erweiterte Schnittstellen enthalten, die das Suffix "Ex" enthalten. Diese Schnittstellen werden von ihren Nicht-Ex-Entsprechungen abgeleitet und enthalten daher alle Funktionen von . Wenn Sie eines der erweiterten Features verwenden möchten, verwenden Sie die Ex-Schnittstellen.

Funktionen, die Zeiger auf BSTRs verwenden, weisen Speicher [**mithilfe von SysAllocString zu.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) Es liegt in der Verantwortung des Aufrufers, diesen Arbeitsspeicher mit [**SysFreeString frei zu geben.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

 

 