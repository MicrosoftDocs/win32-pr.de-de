---
title: Ausrichtungsfehler
description: Ausrichtungsfehler
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- Ausrichtungsfehler bei 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d813a47cb3428c57ee6235442491f26f8d126a997dd7fcfa6844d551e7958b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412910"
---
# <a name="alignment-faults"></a>Ausrichtungsfehler

Der Systemausrichtungs-Fehlerhandler ist auf Itanium-basierten Systemen standardmäßig deaktiviert. Daher generiert jeder nicht ausgerichtete Datenzugriff eine Ausnahme, die nicht automatisch vom System behoben wird, es sei denn, die Anwendung fängt die Ausnahme in einem [framebasierten Ausnahmehandler ab.](/windows/desktop/Debug/frame-based-exception-handling) Um das Systemausrichtungsfehlerhander zu aktivieren, rufen Sie die [**SetErrorMode-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) mit **SEM \_ NOALIGNMENTFAULTEXCEPT auf.** Beachten Sie jedoch, dass prozesse eine schwerwiegende Leistungsbeeinträchtigung feststellen können, wenn der Systemausrichtungs-Fehlerhandler aktiviert ist und der Prozess Ausrichtungsfehler generiert.

Wenn der WinDbg-Debugger als Systemdebugger installiert wurde, wird WinDbg automatisch gestartet, wenn ein Prozess im System eine nicht behandelte Ausnahme generiert. Wenn Sie keinen Debugger als Systemdebugger installiert haben, zeigt das System ein Dialogfeld an, in dem darauf hinweist wird, dass bei Ihrer Anwendung ein Fehler aufgetreten ist, und die Möglichkeit bietet, das Problem an Microsoft zu melden.

Auf x64- und ARM64-Systemen werden alle Ausrichtungsfehler durch eine Kombination aus Hardware und Software behandelt. Um eine optimale Leistung zu erzielen, sollte der Zugriff auf den Arbeitsspeicher ordnungsgemäß ausgerichtet werden. Darüber hinaus sollte der Zugriff auf nicht ausgerichtete [interlocked-Variablen](/windows/desktop/Sync/interlocked-variable-access) auf ARM64 vermieden werden, da diese Vorgänge nicht atomar sind.

 

 