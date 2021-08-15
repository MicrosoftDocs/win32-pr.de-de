---
description: In diesem Thema wird beschrieben, wie Sie einen generischen Experten erstellen, der mit dem Netzwerkmonitor SDK Netzwerkmonitor wird.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Erstellen eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbffc036f27ad0b91fb19906c5f12740919828b33ebfced584e068abe93bd912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064250"
---
# <a name="building-an-expert"></a>Erstellen eines Experten

In diesem Thema wird beschrieben, wie Sie einen generischen Experten erstellen, der mit dem Netzwerkmonitor SDK Netzwerkmonitor wird.

> [!Note]  
> Installieren Sie vor dem Erstellen der folgenden Codebeispiele das Netzwerkmonitor SDK, und initialisieren Sie MySetEnv.bat Datei.

 

**So erstellen Sie einen generischen Experten**

1.  Öffnen Sie Netzwerkmonitor Eingabeaufforderung, und navigieren Sie zum Unterverzeichnis Experts, z. \\ B. C: \\ Programme \\ NetMonSDK2 \\ Experts.
2.  Geben **Sie xcopy /e /s /v Blrplate MyExpert ein.** Geben Sie dann D ein, wenn Sie dazu **aufgefordert werden.**
3.  Wechseln Sie in das \\ Unterverzeichnis MyExpert.
4.  Geben **Sie ren Blrplate \* ein. \* MyExpert \* \* . .** Stellen Sie sicher, dass alle Dateien ordnungsgemäß umbenannt werden. Überprüfen Sie die Dateinamen, indem Sie die Dateien im \\ Unterverzeichnis Experts \\ Blrplate vergleichen.
5.  Bearbeiten Sie das Makefile, indem Sie alle Vorkommen von **Blrplate** durch **MyExpert ersetzen.**
6.  Bearbeiten Sie beide CPP-Dateien, indem Sie alle Vorkommen von **Blrplate** durch **MyExpert ersetzen.** Beachten Sie, dass der Dialogfeldbezeichner in Config.cpp groß groß sein muss (z. B. **MYEXPERT**).
7.  Bearbeiten Sie MyExpert.h, indem Sie alle Vorkommen von **Blrplate** durch **MyExpert ersetzen.**
8.  Bearbeiten Sie Resrc1.h, indem Sie **BLRPLATE in** **MYEXPERT umbenennen.** (Denken Sie daran, **dass MYEXPERT** groß groß sein muss.)
9.  Bearbeiten Sie die Datei MyExpert.rc, indem Sie **IDD \_ BLRPLATE \_ CONFIG \_ DIALOG** in **IDD \_ MYEXPERT \_ CONFIG \_ DIALOG umbenennen.**
10. Geben **Sie nmake ein,** um die DLL-Datei zu erstellen. Wechseln Sie zum Überprüfen des Buildverzeichnisses in das Unterverzeichnis Obj, und überprüfen \\ Sie, ob die Datei vorhanden ist. Weitere Informationen finden Sie unter [Anzeigen von Expert DLL-Eigenschaften.](viewing-expert-dll-properties.md)

Wenn der Build abgeschlossen ist, verfügen Sie über eine erfahrene DLL, die Sie testen und mit Netzwerkmonitor. Weitere Informationen zum Installieren eines Experten finden Sie unter [Installing an Expert to Netzwerkmonitor 2.1](installing-an-expert-to-network-monitor-2-1.md). Weitere Informationen zum Debuggen eines Experten finden Sie unter [Debuggen eines Experten.](debugging-an-expert.md)

 

 



