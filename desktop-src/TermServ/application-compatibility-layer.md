---
title: Anwendungs Kompatibilitäts Ebene
description: Zum Ausführen von Legacy Anwendungen in einer Remotedesktopdienste Umgebung können Sie die Remotedesktopdienste Anwendungs Kompatibilitäts Ebene verwenden.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342368"
---
# <a name="application-compatibility-layer"></a>Anwendungs Kompatibilitäts Ebene

Zum Ausführen von Legacy Anwendungen in einer Remotedesktopdienste Umgebung können Sie die Remotedesktopdienste Anwendungs Kompatibilitäts Ebene verwenden. Wenn der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server eine Anwendung lädt, die nicht Remotedesktopdienste weiß, wird auch eine DLL geladen, die Kompatibilitäts Code enthält. Wenn Sie die Remotedesktopdienste Anwendungs Kompatibilitäts Ebene verwenden möchten, können Sie beim Kompilieren einer Anwendung das Flag nicht TSAWARE festlegen.

Wenn Ihre Anwendung Remotedesktopdienste ist, können Sie den mehr Aufwand für das Laden dieser zusätzlichen dll und das Ausführen des Kompatibilitäts Codes vermeiden.

Wenn Sie angeben möchten, dass Ihre Anwendung Remotedesktopdienste ist, legen Sie das Flag für das **\_ \_ Terminal \_ Server \_ fähige Image dllcharakteristika** im optionalen Header fest. Wenn Sie den Linker verwenden, der mit Microsoft Visual C++ ausgeliefert wird, können Sie dieses Flag mithilfe der **TSAWARE** -Linkeroption festlegen. Das **DUMPBIN** -Tool, das im Lieferumfang von Microsoft Visual C++ enthalten ist, stellt die */Headers* -Option zum Bestimmen des Status des **TSAWARE** -Flags bereit. Weitere Informationen zur Verwendung des **DUMPBIN** -Tools finden Sie unter [DUMPBIN Reference](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Seien Sie vorsichtig, wenn Sie das **TSAWARE** -Flag verwenden, da es der Anwendung ermöglicht, alle Remotedesktopdienste Kompatibilitäts Optimierungen zu umgehen. Das **TSAWARE** -Flag sollte nur verwendet werden, wenn Sie sicher sind, dass Ihre Anwendung für die Remotedesktopdienste Umgebung konzipiert ist. Wenn Ihre Anwendung die folgenden Kriterien erfüllt, können Sie das Flag für **das \_ \_ Terminal \_ Server \_ fähige Image-dllcharakteristika** auf sichere Weise verwenden.

-   Die Anwendung verwendet keine INI-Dateien.
-   Die Anwendung schreibt während des Setups nicht in den **aktuellen HKEY- \_ \_ Benutzer** . Weitere Informationen finden Sie unter [Speichern von User-Specific Informationen](storing-user-specific-information.md).
-   Die Anwendung wird nicht als Systemdienst ausgeführt (d. h. LUID = System).
-   Die Anwendung erwartet nicht exklusiven Zugriff auf die Windows-oder andere Systemverzeichnisse. Dies bedeutet, dass die Anwendung keine temporären oder Konfigurationsdaten pro Benutzer in den Windows-oder anderen Systemverzeichnissen speichert.
-   Die Anwendung schreibt nicht in die Registrierungs Struktur des **lokalen HKEY** -Computers, um benutzerspezifische Daten oder Konfigurationen zu erstellen.
-   Die Anwendung befolgt andere Remotedesktopdienste Kompatibilitätsrichtlinien, die in diesem Dokument erwähnt werden.

 

 