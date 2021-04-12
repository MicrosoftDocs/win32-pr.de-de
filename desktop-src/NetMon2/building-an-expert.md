---
description: In diesem Thema wird beschrieben, wie ein generischer Experte erstellt wird, der mit dem Netzwerkmonitor SDK ausgeliefert wird.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Entwickeln eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215892"
---
# <a name="building-an-expert"></a>Entwickeln eines Experten

In diesem Thema wird beschrieben, wie ein generischer Experte erstellt wird, der mit dem Netzwerkmonitor SDK ausgeliefert wird.

> [!Note]  
> Installieren Sie vor dem Erstellen der folgenden Codebeispiele das Netzwerkmonitor SDK, und initialisieren Sie die Datei MySetEnv.bat.

 

**So erstellen Sie einen generischen Experten**

1.  Öffnen Sie eine Netzwerkmonitor Eingabeaufforderung, und navigieren Sie zum \\ Unterverzeichnis Experts, z. b \\ . C: Program Files \\ NetMonSDK2 \\ Experten.
2.  Type **xcopy/e/s/v blrplate myexpert**; Wenn Sie dazu aufgefordert werden, geben Sie **D** ein.
3.  Wechseln Sie zum \\ Unterverzeichnis myexpert.
4.  Geben Sie **ren blrplate ein \* . \* Myexpert \* . \***. Stellen Sie sicher, dass alle Dateien ordnungsgemäß umbenannt wurden. Überprüfen Sie die Dateinamen, indem Sie die Dateien im \\ \\ Unterverzeichnis "Experten blrplate" vergleichen.
5.  Bearbeiten Sie das Makefile, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen.
6.  Bearbeiten Sie beide cpp-Dateien, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen. Beachten Sie, dass der Dialogfeld Bezeichner in der Datei "config. cpp" groß geschrieben werden muss (z. b. **myexpert**).
7.  Bearbeiten Sie myexpert. h, indem Sie alle Vorkommen von **blrplate** durch **myexpert** ersetzen.
8.  Bearbeiten Sie Resrc1. h durch Umbenennen von **blrplate** in **myexpert** (Beachten Sie, dass **myexpert** groß geschrieben werden muss.)
9.  Bearbeiten Sie die Datei myexpert. RC, indem Sie **IDD \_ blrplate \_ config \_ Dialog** in **IDD \_ myexpert \_ config \_ Dialog** umbenennen.
10. Geben Sie **NMAKE** ein, um die DLL-Datei zu erstellen. Wechseln Sie zum Überprüfen des Builds in das \\ obj-Unterverzeichnis, und überprüfen Sie, ob die Datei vorhanden ist. Weitere Informationen finden Sie unter [Anzeigen von Eigenschaften der expertendll](viewing-expert-dll-properties.md).

Nachdem der Build fertiggestellt wurde, verfügen Sie über eine Experten-dll, die Sie mit Netzwerkmonitor testen und bereitstellen können. Weitere Informationen zum Installieren eines Experten finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md). Weitere Informationen zum Debuggen eines Experten finden Sie unter [Debuggen eines Experten](debugging-an-expert.md).

 

 



