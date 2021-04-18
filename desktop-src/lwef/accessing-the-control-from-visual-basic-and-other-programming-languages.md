---
title: Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen
description: Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45854b55b3826354543411c44dcd21d9f1d77e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340845"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Sie können auch die Kontrolle des Microsoft-Agents aus Visual Basic und anderen Programmiersprachen verwenden. Stellen Sie sicher, dass die Sprache die ActiveX-Steuerelement Schnittstelle vollständig unterstützt und den Konventionen zum Hinzufügen und Zugreifen auf ActiveX-Steuerelemente folgt. Der-Agent muss bereits auf dem Zielsystem installiert sein, um auf das-Steuerelement zugreifen zu können.

Anschließend können Sie die selbst installierbare CAB-Datei des Agents von der Website herunterladen (mit der Option "Speichern" anstelle von "ausführen"). Sie können diese Datei in das Setup Programm für die Installation einschließen. Wenn er ausgeführt wird, wird der-Agent automatisch auf dem Zielsystem installiert. Weitere Informationen zur Installation finden Sie unter Microsoft Agent Distribution License Agreement. Die Installation außer der selbst installierenden CAB-Datei des Agents (z. b. der Versuch, agentkomponentendateien zu kopieren und zu registrieren) wird nicht unterstützt. Dadurch wird eine konsistente und umfassende Installation sichergestellt. Beachten Sie, dass die selbst Installationsdatei des Microsoft-Agents nicht unter Microsoft Windows 2000 installiert wird, da diese Version des Betriebssystems bereits eine eigene Version des Agents enthält.

Wenn Sie den-Agent erfolgreich auf einem Zielsystem installieren möchten, müssen Sie auch sicherstellen, dass das Zielsystem über eine aktuelle Version der Microsoft Visual C++ Runtime (Msvcrt.dll), des Microsoft-Registrierungs Tools (Regsvr32.dll) und der Microsoft com-DLLs verfügt. Die einfachste Möglichkeit, um sicherzustellen, dass die erforderlichen Komponenten auf dem Zielsystem installiert sind, besteht darin, dass Microsoft Internet Explorer 3,02 oder höher installiert ist. Alternativ können Sie die ersten beiden Komponenten installieren, die als Teil Microsoft Visual C++ verfügbar sind. Die erforderlichen COM-DLLs können als Teil des Microsoft DCOM-Updates installiert werden, das auf der Microsoft-Website verfügbar ist. Weitere Informationen und Lizenzierungsinformationen zu diesen Komponenten finden Sie auf der Microsoft-Website.

Die Sprachkomponenten des Agents können auf die gleiche Weise installiert werden. Auf ähnliche Weise können Sie diese Technik verwenden, um das ACS-Format der Microsoft-Zeichen zu installieren, die für die Verteilung auf der Microsoft Agent-Website verfügbar sind. Die Zeichen Dateien werden automatisch im Unterverzeichnis Microsoft-Agent- \\ chars installiert.

Da die Komponenten des Microsoft-Agents als Betriebssystemkomponenten entworfen wurden, ist der-Agent möglicherweise nicht deinstalliert. Ebenso, wo der-Agent bereits als Teil des Windows-Betriebssystems installiert ist, kann die CAB-Datei des Agents möglicherweise nicht installiert werden.

 

 




