---
title: Anwendungskompatibilitätsschicht
description: Zum Ausführen von Legacyanwendungen in einer Remotedesktopdienste können Sie die Remotedesktopdienste Anwendungskompatibilitätsebene verwenden.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3630346578801e4d2578db6f528048914412dc9ad1a8544e2c2d303188814b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099610"
---
# <a name="application-compatibility-layer"></a>Anwendungskompatibilitätsschicht

Zum Ausführen von Legacyanwendungen in einer Remotedesktopdienste können Sie die Remotedesktopdienste Anwendungskompatibilitätsebene verwenden. Wenn der Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) eine Anwendung lädt, die nicht Remotedesktopdienste ist, lädt er auch eine DLL, die Kompatibilitätscode enthält. Um die Remotedesktopdienste Anwendungskompatibilitätsebene zu verwenden, können Sie beim Kompilieren einer Anwendung das NOT TSAWARE-Flag festlegen.

Wenn Ihre Anwendung Remotedesktopdienste ist, können Sie den Mehraufwand vermeiden, der durch das Laden dieser zusätzlichen DLL und das Ausführen des Kompatibilitätscodes verursacht wird.

Um anzugeben, dass Ihre Anwendung Remotedesktopdienste ist, legen Sie das **FLAG IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE** im optionalen Header fest. Wenn Sie den Linker verwenden, der im Microsoft Visual C++ ist, können Sie dieses Flag mithilfe der **TSAWARE-Linkeroption** festlegen. Das **dumpbin-Tool,** das mit Microsoft Visual C++, stellt die *Option /HEADERS* zur Verfügung, um den Status des **TSAWARE-Flags zu** bestimmen. Weitere Informationen zur Verwendung des **DUMPBIN-Tools** finden Sie unter [DUMPBIN-Referenz.](/cpp/build/reference/dumpbin-reference?view=vs-2019)

Seien Sie vorsichtig, wenn Sie das **TSAWARE-Flag** verwenden, da es Ihrer Anwendung ermöglicht, alle Remotedesktopdienste Kompatibilitätsoptimierungen zu umgehen. Das **TSAWARE-Flag** sollte nur verwendet werden, wenn Sie sicher sind, dass Ihre Anwendung für die Remotedesktopdienste ist. Wenn Ihre Anwendung die folgenden Kriterien erfüllt, können Sie das **FLAG IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER AWARE \_ \_ sicher** verwenden.

-   Die Anwendung verwendet keine .ini Dateien.
-   Die Anwendung schreibt während des Setups nicht **in HKEY \_ CURRENT \_ USER.** Weitere Informationen finden Sie unter [Speichern User-Specific Information.](storing-user-specific-information.md)
-   Die Anwendung wird nicht als Systemdienst (d. h. LUID=System) ausgeführt.
-   Die Anwendung erwartet keinen exklusiven Zugriff auf Windows oder andere Systemverzeichnisse. Dies bedeutet, dass die Anwendung keine temporären oder Konfigurationsdaten pro Benutzer im Windows oder anderen Systemverzeichnissen gespeichert.
-   Die Anwendung schreibt für benutzerspezifische Daten oder Konfigurationen nicht in die Registrierungsstruktur des lokalen **HKEY-Computers.**
-   Die Anwendung folgt anderen Remotedesktopdienste in diesem Dokument erwähnten Kompatibilitätsrichtlinien.

 

 