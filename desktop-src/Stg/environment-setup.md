---
title: Einrichten der Umgebung
description: Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei im Stammverzeichnis des Platform SDK bereit, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen einzurichten, die das Platform SDK verwenden.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341851"
---
# <a name="environment-setup"></a>Einrichten der Umgebung

Das installierte Platform Software Development Kit (SDK) stellt eine Setenv.bat-Datei im Stammverzeichnis des Platform SDK bereit, das Sie ausführen können, um Ihre Umgebung für die Entwicklung von Anwendungen einzurichten, die das Platform SDK verwenden.

## <a name="settings-and-variables"></a>Einstellungen und Variablen

Sie können Ihre Umgebung auch manuell einrichten, indem Sie Ihrer Autoexec.bat-Datei etwas wie das folgende hinzufügen. Mithilfe von Windows können Sie die Autoexec.bat Datei bearbeiten, um diese Befehle einzubeziehen. Mithilfe von Windows Server 2003, Windows XP, Windows 2000 oder Windows NT können Sie diese Einstellungen mithilfe des System Dialogfelds, das Sie in der Systemsteuerung ausführen können, den Umgebungsvariablen bearbeiten oder hinzufügen.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Diese Einstellungen sind für eine Plattform von Intel 80386 oder höher geeignet, auf der Windows Me, Windows 98 oder Windows 95 ausgeführt wird und auf denen sowohl Microsoft Visual C++ als auch das Platform SDK installiert sind. Beispielsweise wird auf diesem System Visual C++ Version 5,0 unter dem Verzeichnis C: \\ Msdev installiert. Das Platform SDK wird unter dem Verzeichnis "D: \\ Mssdk" installiert. Die Datenträger Konfiguration ist möglicherweise anders. Die Platform SDK-Verzeichnisse (in diesem Beispiel mit "D: \\ Mssdk") sind alle zuvor in jeder Pfad Sequenz. Diese Sequenz geht davon aus, dass Befehlszeilen Kompilierungen im Eingabe Aufforderungs Fenster ausgeführt werden sollen und dass die. h-Bibliotheksdateien include und. lib im Platform SDK für diese Kompilierungen bevorzugt werden.

Die CPU-Umgebungsvariable wird definiert, um die Win32-Builds abhängig von der Plattform zu steuern. Zu den aktuell möglichen Werten zählen i386, mips, Alpha und PPC. Weitere Informationen finden Sie in der Datei Win32. MAK, die im Platform SDK im \\ Verzeichnis "Mssdk include" bereitgestellt wird \\ . Alle Codebeispiele für com-Tutorial enthalten Win32. MAK.

 

 




