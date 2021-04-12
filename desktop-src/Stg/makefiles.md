---
title: Makefiles
description: Die Makefiles für jedes der Codebeispiele in dieser Reihe sind generische Microsoft-Win32-Makefiles und sollen über das Eingabe Aufforderungs Fenster erstellt werden.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Makefiles strukturierte Speicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311580"
---
# <a name="makefiles"></a>Makefiles

Die Makefiles für jedes der Codebeispiele in dieser Reihe sind generische Microsoft-Win32-Makefiles und sollen über das Eingabe Aufforderungs Fenster erstellt werden. Sie setzen die Microsoft Compiler-und Linkertools voraus und benötigen ggf. einige Änderungen, damit Sie mit anderen Tools funktionieren. Die meisten Compiler/Linker-Befehls Zeilenschalter werden durch Makros angegeben, die in der im Platform Software Development Kit (SDK) enthaltenen Datei "Win32. MAK Makefile" definiert sind.

Die Makeall.bat-Datei und die jeweiligen Codebeispiel Makefile unterstützen die in der folgenden Tabelle aufgeführten allgemeinen Optionen für den Aufruf im Eingabe Aufforderungs Fenster, um die Art des Builds zu steuern.



| NMAKE-Aufruf        | Makeall-Aufruf          | Wirkung                       |
|-------------------------|-----------------------------|------------------------------|
| **NMAKE**               | **makeall**                 | Kompilieren mit Debuginformationen.     |
| **NMAKE** **NoDebug = 1** | **makeall** **"NoDebug = 1"** | Kompilieren ohne Debuginformationen.  |
| **NMAKE** - **Profil = 1** | **makeall** **"Profile = 1"** | Mit Profil Erstellungs Informationen kompilieren. |
| **NMAKE** **Tune = 1**    | **makeall** **"Tune = 1"**    | Mit Arbeits Satz-Tuner-Informationen. |
| **NMAKE** **Unicode = 1** | **makeall** **"Unicode = 1"** | Kompilieren Sie für Unicode.         |
| **NMAKE** **Bereinigen**     | **makeall** **bereinigt**       | Löschen Sie temporäre Binärdateien.   |
| **NMAKE** **cleanall**  | **makeall** - **cleanall**    | Löschen Sie alle generierten Dateien.  |



 

Bei den Makeall.bat aufrufen müssen die Anführungszeichen wie angezeigt werden. Die Optionen " **NoDebug**", " **profile**" und " **Tune** " schließen sich gegenseitig aus: Sie dürfen für eine bestimmte Kompilierung/Verknüpfung nur eine oder keine verwenden. Um die Beispiele zum Ausführen mit Unicode-Zeichen folgen zu kompilieren, verwenden Sie die Option **"Unicode = 1"** . Der Standardwert ist die Kompilierung für die herkömmliche Unterstützung von ANSI-Zeichen folgen, da Sie dann unter einem beliebigen 32-Bit-Windows-Betriebssystem ausführen können. Sie können mit oder ohne Unicode auf Windows Server 2003 und höher und Windows 2000 und höher kostenlos kompilieren und ausführen. Beachten Sie, dass apputil immer mit denselben Optionen wie die anderen Codebeispiele kompiliert wird, die separat kompiliert werden können. Dies gilt insbesondere für die Option **"Unicode = 1"** .

Sie können eine installierte 32-Bit-IDE (C++ Integrated Development Environment, integrierte Entwicklungsumgebung) verwenden, um die Beispiele mit den bereitgestellten generischen Makefiles zu erstellen. Hierfür ist es erforderlich, dass Sie in Ihrer IDE die generischen Makefiles als ' externe ' Makefiles verarbeiten. Die bereitgestellten Makefiles erfordern ein Microsoft NMAKE-kompatibles Make-Hilfsprogramm.

Die meisten C++-IDES können diese Makefiles als extern erkennen und dennoch viele "Edit-Build-Debug"-Vorteile der IDE bereitstellen. Beispielsweise können Sie in Microsoft Visual Studio 97 oder höher im Menü Datei die Option Arbeitsbereich öffnen auswählen, um einen Arbeitsbereich zu schaffen, indem Sie eine ordnungsgemäß benannte Kopie (z. b. exeskel. MAK) des Code Beispiels Win32 Makefile öffnen.

 

 




