---
description: Die schreibgeschützte modulekeys-Eigenschaft des Error-Objekts gibt einen Zeiger auf eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Zeile im Modul enthält, die den Fehler verursacht hat, einen Schlüssel pro Eintrag in der Auflistung.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Error. modulekeys-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360359"
---
# <a name="errormodulekeys-property"></a>Error. modulekeys (Eigenschaft)

Die schreibgeschützte **modulekeys** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt einen Zeiger auf eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Zeile im Modul enthält, die den Fehler verursacht hat, einen Schlüssel pro Eintrag in der Auflistung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Client ist für das Freigeben der Zeichen folgen Auflistung verantwortlich, wenn er nicht mehr benötigt wird.

Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ modulekeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

