---
description: Initialisiert die \_ Hilfsbibliothek .
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: AuxKlibInitialize-Funktion \_ (Aux-Funktion "Aux"-Datei ".h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654880"
---
# <a name="auxklibinitialize-function"></a>AuxKlibInitialize-Funktion

Initialisiert die \_ Hilfsbibliothek . Diese Funktion muss aufgerufen werden, bevor eine andere Funktion in der Bibliothek aufgerufen werden kann.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert STATUS \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der status-Codes sein, die in Ntstatus.h definiert sind, der im WDK verfügbar ist.

## <a name="remarks"></a>Hinweise

Die Objektbibliothek, die diese API implementiert, kann hier heruntergeladen [werden.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|------------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Zusätzliche API-Bibliothek, Version 1.0 oder höher<br/>                            |
| Header<br/>          | <dl> <dt>\_Aux-Datei ".h"</dt> </dl>   |
| Bibliothek<br/>         | <dl> <dt>\_Aux-Datei "Aux"-Datei ".lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




