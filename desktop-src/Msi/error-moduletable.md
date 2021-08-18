---
description: Die schreibgeschützte ModuleTable-Eigenschaft gibt den Namen der Tabelle im Modul zurück, die den Fehler verursacht hat.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Error.ModuleTable-Eigenschaft (Mergemod.h)
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
ms.openlocfilehash: 47cd9bab5c12230a048da04e60169e1ad21195df2304642f6b656983539f3b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947072"
---
# <a name="errormoduletable-property"></a>Error.ModuleTable-Eigenschaft

Die schreibgeschützte **ModuleTable-Eigenschaft** gibt den Namen der Tabelle im Modul zurück, die den Fehler verursacht hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp angewendet werden. Sie können den Fehlertyp ermitteln, indem Sie die [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts**](error-object.md) aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden Sie unter Get ModuleTable function (Abrufen der [**\_ ModuleTable-Funktion).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

