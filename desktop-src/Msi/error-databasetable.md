---
description: Die schreibgeschützte DatabaseTable-Eigenschaft des Error-Objekts gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Error.DatabaseTable-Eigenschaft (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b9e52523b37c90de4c4592fdeb059e6269f4e05e240242e69e14f0be6d4d53a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378171"
---
# <a name="errordatabasetable-property"></a>Error.DatabaseTable-Eigenschaft

Die schreibgeschützte **DatabaseTable-Eigenschaft** des [**Error-Objekts**](error-object.md) gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp angewendet werden. Sie können den Fehlertyp ermitteln, indem Sie die [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts**](error-object.md) aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden Sie unter Abrufen der [**\_ DatabaseTable-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

