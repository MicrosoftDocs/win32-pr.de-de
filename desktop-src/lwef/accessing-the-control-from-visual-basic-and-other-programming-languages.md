---
title: Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen
description: Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976860"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Zugreifen auf das Steuerelement über Visual Basic und andere Programmiersprachen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Sie können das -Steuerelement von Microsoft Agent auch über Visual Basic anderen Programmiersprachen verwenden. Stellen Sie sicher, dass die Sprache die ActiveX-Steuerelementschnittstelle vollständig unterstützt, und befolgen Sie die Konventionen zum Hinzufügen und Zugreifen auf ActiveX Steuerelementen. Für den Zugriff auf das Steuerelement muss der -Agent bereits auf dem Zielsystem installiert sein.

Sie können dann die selbstinstallierende Cabinet-Datei des Agents von der Website herunterladen (mithilfe der Option Speichern anstelle von Ausführen). Sie können diese Datei in Das Setupprogramm für die Installation verwenden. Bei jeder Ausführung wird der -Agent automatisch auf dem Zielsystem installiert. Weitere Informationen zur Installation finden Sie im Microsoft Agent-Verteilungslizenzvertrag. Eine andere Installation als die Verwendung der selbstinstallierenDentinstallationsdatei des -Agents, z. B. der Versuch, Agent-Komponentendateien zu kopieren und zu registrieren, wird nicht unterstützt. Dadurch wird eine konsistente und vollständige Installation sichergestellt. Beachten Sie, dass die Selbstinstallierungsdatei von Microsoft Agent nicht unter Microsoft Windows 2000 installiert wird, da diese Version des Betriebssystems bereits eine eigene Version des -Agents enthält.

Um den -Agent erfolgreich auf einem Zielsystem zu installieren, müssen Sie auch sicherstellen, dass das Zielsystem über eine aktuelle Version der Microsoft Visual C++-Runtime (Msvcrt.dll), des Microsoft-Registrierungstool (Regsvr32.dll) und der Microsoft COM-DLLs verfügt. Die einfachste Möglichkeit, sicherzustellen, dass sich die erforderlichen Komponenten auf dem Zielsystem befinden, besteht in der Installation von Microsoft Internet Explorer 3.02 oder höher. Alternativ können Sie die ersten beiden Komponenten installieren, die als Teil des Microsoft Visual C++. Die erforderlichen COM-DLLs können als Teil des Microsoft DCOM-Updates installiert werden, das auf der Microsoft-Website verfügbar ist. Weitere Informationen und Lizenzierungsinformationen für diese Komponenten finden Sie auf der Microsoft-Website.

Die Sprachkomponenten des Agents können auf die gleiche Weise installiert werden. Auf ähnliche Weise können Sie dieses Verfahren verwenden, um das ACS-Format der Microsoft-Zeichen zu installieren, die für die Verteilung über die Microsoft Agent-Website verfügbar sind. Die Zeichendateien werden automatisch im Microsoft Agent \\ Chars-Unterverzeichnis installiert.

Da die Komponenten von Microsoft Agent als Betriebssystemkomponenten entworfen wurden, wird der -Agent möglicherweise nicht deinstalliert. Wenn der -Agent bereits als Teil des betriebssystembasierten Windows installiert ist, wird der selbstinstallierte Agent-Schaltet möglicherweise nicht installiert.

 

 




