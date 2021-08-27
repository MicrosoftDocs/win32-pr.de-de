---
description: Manchmal ist es erforderlich, eine DLL durch eine neuere Version zu ersetzen.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link Bibliotheksupdates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f294e16efac60da843c14d200aaa768d4fc78ce8a922cb0aa6958756a9903be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075540"
---
# <a name="dynamic-link-library-updates"></a>Dynamic-Link Bibliotheksupdates

Manchmal ist es erforderlich, eine DLL durch eine neuere Version zu ersetzen. Führen Sie vor dem Ersetzen einer DLL eine Versionsprüfung durch, um sicherzustellen, dass Sie eine ältere Version durch eine neuere Version ersetzen. Es ist möglich, eine dll zu ersetzen, die verwendet wird. Welche Methode Sie verwenden, um die verwendeten DLLs zu ersetzen, hängt vom verwendeten Betriebssystem ab. Auf Windows XP und höher sollten Anwendungen [isolierte Anwendungen und assemblyseitige Assemblys](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)verwenden.

Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie die folgenden Schritte ausführen:

1.  Verwenden Sie die [**MoveFileEx-Funktion,**](/windows/desktop/api/winbase/nf-winbase-movefileexa) um die zu ersetzende DLL umzubenennen. Geben Sie MOVEFILE COPY ALLOWED nicht \_ \_ an, und stellen Sie sicher, dass sich die umbenannte Datei auf demselben Volume befindet, das die ursprüngliche Datei enthält. Sie können die Datei auch einfach im gleichen Verzeichnis umbenennen, indem Sie ihr eine andere Erweiterung geben.
2.  Kopieren Sie die neue DLL in das Verzeichnis, das die umbenannte DLL enthält. Alle Anwendungen verwenden jetzt die neue DLL.
3.  Verwenden Sie [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) mit MOVEFILE \_ DELAY UNTIL \_ \_ REBOOT, um die umbenannte DLL zu löschen.

Bevor Sie diese Ersetzung vornehmen, verwenden Anwendungen die ursprüngliche DLL, bis sie entladen wird. Nachdem Sie den Ersatz erstellt haben, verwenden Anwendungen die neue DLL. Wenn Sie eine DLL schreiben, müssen Sie darauf achten, dass sie für diese Situation vorbereitet ist, insbesondere wenn die DLL globale Statusinformationen verwaltet oder mit anderen Diensten kommuniziert. Wenn die DLL nicht auf eine Änderung der globalen Zustandsinformationen oder Kommunikationsprotokolle vorbereitet ist, müssen Sie beim Aktualisieren der DLL den Computer neu starten, um sicherzustellen, dass alle Anwendungen die gleiche Version der DLL verwenden.

 

 
