---
title: Einrichten der Umgebung
description: Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei bereit, die sich im Stammverzeichnis des Platform SDK befindet, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen, die das Platform SDK verwenden, einrichten.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b7de27bfc015726786011376c821c5ae0e86a07d95f03098ed376dd022cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739390"
---
# <a name="environment-setup"></a>Einrichten der Umgebung

Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei bereit, die sich im Stammverzeichnis des Platform SDK befindet, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen, die das Platform SDK verwenden, einrichten.

## <a name="settings-and-variables"></a>Einstellungen und Variablen

Sie können Ihre Umgebung auch manuell einrichten, indem Sie ihrer Datei die folgende Autoexec.bat hinzufügen. Mit Windows können Sie die Autoexec.bat bearbeiten, um diese Befehle ein beispielsend zu verwenden. Mithilfe von Windows Server 2003, Windows XP, Windows 2000 oder Windows NT können Sie diese Einstellungen mithilfe des Dialogfelds System bearbeiten oder Ihren Umgebungsvariablen hinzufügen, das Sie über die Systemsteuerung.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Diese Einstellungen sind für eine Intel 80386- oder höher-Plattform geeignet, auf der Windows Me, Windows 98 oder Windows 95 ausgeführt wird, auf der sowohl Microsoft Visual C++ als auch das Platform SDK installiert sind. Auf diesem System wird beispielsweise Visual C++ 5.0 im Verzeichnis C: \\ MSDEV installiert. Das Platform SDK wird unter dem Verzeichnis D: \\ MSSDK installiert. Ihre Datenträgerkonfiguration kann sich unterscheiden. Die Platform SDK-Verzeichnisse (in diesem Beispiel die verzeichnisse mit D: \\ MSSDK) sind alle früher in jeder Pfadsequenz. Bei dieser Sequenz wird davon ausgegangen, dass Befehlszeilenkompilierungen im Eingabeaufforderungsfenster ausgeführt werden sollen und dass die .h-Include- und LIB-Bibliotheksdateien im Platform SDK für diese Kompilierungen bevorzugt werden.

Die CPU-Umgebungsvariable wird definiert, um die Win32-Builds abhängig von der Plattform zu steuern. Aktuelle mögliche Werte sind i386, MIPS, ALPHA und PPC. Weitere Informationen finden Sie in der Datei Win32.mak, die im Platform SDK im \\ MSSDK \\ INCLUDE-Verzeichnis bereitgestellt wird. Alle Makefiles für das COM-Tutorialcodebeispiel enthalten Win32.mak.

 

 




