---
description: Bestimmt, ob sich der Terminalserver im INSTALLATIONSmodus befindet.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f6bf6408fb7bd72b1757b8ca2219e1bbd2cc612829359fdcaf090786e8e7e98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570890"
---
# <a name="termsrvappinstallmode-function"></a>TermsrvAppInstallMode-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden. Sie kann sich ohne vorherige Ankündigung ändern oder vollständig verschwinden.\]

Bestimmt, ob sich der Terminalserver im INSTALLATIONSmodus befindet.

## <a name="syntax"></a>Syntax


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sich der Terminalserver im INSTALLATIONSmodus befindet, und **FALSE,** wenn er sich im EXECUTE-Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




