---
title: _allmul-Routine
description: Multipliziert zwei ganze Zahlen vom Typ "Longlong" oder "ULONGLONG".
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104038469"
---
# <a name="_allmul-routine"></a>\_allmul-Routine

Multipliziert zwei ganze Zahlen vom Typ " **Longlong** " oder " **ULONGLONG** ".
Um z. b. zwei Int64-Werte zu multiplizieren, generiert der Compiler möglicherweise einen-Rückruf für die **\_ allmul** -Routine.

## <a name="remarks"></a>Bemerkungen

Die **\_ allmul** -Routine ist eine Hilfsroutine für den C-Compiler.
Ob der Compiler **\_ allmul** verwendet, ist vollständig vom Optimierungs Satz abhängig.

Diese Routine wird nur auf x86-Plattformen verwendet.
