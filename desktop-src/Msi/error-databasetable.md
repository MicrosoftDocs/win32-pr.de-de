---
description: Die schreibgeschützte databasetable-Eigenschaft des Error-Objekts gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Error. databasetable-Eigenschaft (Mergemod. h)
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
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369524"
---
# <a name="errordatabasetable-property"></a>Error. databasetable-Eigenschaft

Die schreibgeschützte **databasetable** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ databasetable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

