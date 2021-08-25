---
description: Die schreibgeschützte Language-Eigenschaft des Error-Objekts gibt die LANGID des aktuellen Fehlers zurück.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Error.Language-Eigenschaft (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082890"
---
# <a name="errorlanguage-property"></a>Error.Language(Eigenschaft)

Die schreibgeschützte **Language-Eigenschaft** des [**Error-Objekts**](error-object.md) gibt die **LANGID** des aktuellen Fehlers zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Der Wert der **Language-Eigenschaft** ist -1, es sei denn, der Fehler ist vom Typ msmErrorLanguageUnsupported oder msmErrorLanguageFailed. Sie können den Fehlertyp ermitteln, indem Sie die [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts**](error-object.md) aufrufen.

### <a name="c"></a>C++

Weitere Informationen [**finden Sie unter get Language Function \_ (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

