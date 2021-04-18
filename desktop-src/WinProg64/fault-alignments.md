---
title: Ausrichtungsfehler
description: Ausrichtungsfehler
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- Ausrichtungsfehler 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338485"
---
# <a name="alignment-faults"></a>Ausrichtungsfehler

Der System Ausrichtungsfehler Handler ist auf Itanium-basierten Systemen standardmäßig deaktiviert. Daher wird durch den nicht ausgerichteten Datenzugriff eine Ausnahme generiert, die nicht automatisch vom System korrigiert wird, es sei denn, die Anwendung fängt die Ausnahme in einem [Frame basierten Ausnahmehandler](/windows/desktop/Debug/frame-based-exception-handling)ab. Um den systemausrichtungs-Fault-Handler zu aktivieren, müssen Sie [**die Funktion "**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) *" mit " **SEM \_ noalignmentfaultexcept**" aufrufen. Beachten Sie jedoch, dass es bei Prozessen zu schwerwiegenden Leistungseinbußen kommen kann, wenn der System Ausrichtungsfehler Handler aktiviert ist und der Prozess Ausrichtungsfehler generiert.

Wenn der WinDbg-Debugger als System Debugger installiert wurde, wird WinDBG automatisch gestartet, wenn ein Prozess im System eine nicht behandelte Ausnahme generiert. Wenn Sie keinen Debugger als System Debugger installiert haben, zeigt das System ein Dialogfeld an, in dem Sie darauf hingewiesen werden, dass die Anwendung einen Fehler festgestellt hat und die Gelegenheit bietet, das Problem an Microsoft zu melden.

Auf x64-und ARM64-Systemen werden alle Ausrichtungsfehler durch eine Kombination aus Hardware und Software behandelt. Für eine optimale Leistung sollte der gesamte Zugriff auf den Arbeitsspeicher ordnungsgemäß ausgerichtet werden. Außerdem sollte der nicht ausgerichtete [Zugriff auf Interlocked-Variablen](/windows/desktop/Sync/interlocked-variable-access) auf ARM64 vermieden werden, da diese Vorgänge nicht atomarisch sind.

 

 