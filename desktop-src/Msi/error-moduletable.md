---
description: Die schreibgeschützte moduletable-Eigenschaft gibt den Namen der Tabelle im Modul zurück, das den Fehler verursacht hat.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Error. moduletable-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369620"
---
# <a name="errormoduletable-property"></a>Error. moduletable (Eigenschaft)

Die Schreib **geschützte moduletable** -Eigenschaft gibt den Namen der Tabelle im Modul zurück, das den Fehler verursacht hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ moduletable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

