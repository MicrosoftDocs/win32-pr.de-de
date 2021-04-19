---
description: Initialisiert die aux \_ KLIB-Bibliothek.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Funktion "auxklibinitialize" (AUX \_ KLIB. h)
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
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369227"
---
# <a name="auxklibinitialize-function"></a>Funktion "auxklibinitialize"

Initialisiert die aux \_ KLIB-Bibliothek. Diese Funktion muss aufgerufen werden, bevor eine andere Funktion in der Bibliothek aufgerufen werden kann.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der in "NTSTATUS. h" definierten Statuscodes sein, die im WDK verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|------------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher<br/>                            |
| Header<br/>          | <dl> <dt>AUX \_ KLIB. h</dt> </dl>   |
| Bibliothek<br/>         | <dl> <dt>AUX \_ KLIB. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Auxklibquerymoduleinformation"**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




