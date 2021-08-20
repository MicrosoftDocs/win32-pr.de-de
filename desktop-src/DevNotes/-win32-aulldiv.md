---
title: _aulldiv Routine
description: Dividiert zwei ULONGLONG-Ganzzahlen.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538900"
---
# <a name="_aulldiv-routine"></a>\_aulldiv Routine

Dividiert zwei **ULONGLONG-Ganzzahlen.**
Um beispielsweise zwei uint64-Werte zu teilen, generiert der Compiler möglicherweise einen Aufruf der Routine **\_ aulldiv.**

## <a name="remarks"></a>Hinweise

Die Routine **\_ aulldiv** ist eine Hilfsroutine für den C-Compiler.
Ob der Compiler **\_ aulldiv verwendet,** hängt vollständig vom Optimierungssatz ab.

Diese Funktion wird nur auf x86-Plattformen verwendet.
