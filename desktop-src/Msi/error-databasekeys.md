---
description: Die schreibgeschützte databasekeys-Eigenschaft des Error-Objekts gibt eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht hat. In der Sammlung ist ein Schlüssel pro Eintrag vorhanden.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Error. databasekeys-Eigenschaft (Mergemod. h)
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
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373576"
---
# <a name="errordatabasekeys-property"></a>Error. databasekeys (Eigenschaft)

Die schreibgeschützte **databasekeys** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht hat. In der Sammlung ist ein Schlüssel pro Eintrag vorhanden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Client ist für das Freigeben der Zeichen folgen Auflistung verantwortlich, wenn er nicht mehr benötigt wird.

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ databasekeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

