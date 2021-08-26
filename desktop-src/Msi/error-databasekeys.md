---
description: Die schreibgeschützte DatabaseKeys-Eigenschaft des Error-Objekts gibt eine Zeichenfolgensammlung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht. Es gibt einen Schlüssel pro Eintrag in der Auflistung.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Error.DatabaseKeys-Eigenschaft (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 075fba028dd045c831adb84a7133fd524398fc74037b7e3c31116b76a4c95a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086040"
---
# <a name="errordatabasekeys-property"></a>Error.DatabaseKeys(Eigenschaft)

Die schreibgeschützte **DatabaseKeys-Eigenschaft** des [**Error-Objekts**](error-object.md) gibt eine Zeichenfolgensammlung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht. Es gibt einen Schlüssel pro Eintrag in der Auflistung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Der Client ist für die Freigabe der Zeichenfolgensammlung verantwortlich, wenn sie nicht mehr benötigt wird.

Die Auflistung ist leer, wenn die Werte nicht für den Fehlertyp gelten. Sie können den Fehlertyp ermitteln, indem Sie die [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts**](error-object.md) aufrufen.

### <a name="c"></a>C++

Siehe [**get \_ DatabaseKeys-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

