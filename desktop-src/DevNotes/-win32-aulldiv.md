---
title: _aulldiv-Routine
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
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104472204"
---
# <a name="_aulldiv-routine"></a>\_aulldiv-Routine

Dividiert zwei **ULONGLONG** -Ganzzahlen.
Wenn Sie z. b. zwei UInt64-Werte aufteilen möchten, generiert der Compiler möglicherweise einen-Rückruf der **\_ aulldiv** -Routine.

## <a name="remarks"></a>Bemerkungen

Die **\_ aulldiv** -Routine ist eine Hilfsroutine für den C-Compiler.
Ob der Compiler **\_ aulldiv** verwendet, ist vollständig von der Optimierungs Gruppe abhängig.

Diese Funktion wird nur auf x86-Plattformen verwendet.
