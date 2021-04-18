---
description: Die schreibgeschützte Language-Eigenschaft des Error-Objekts gibt die langid des aktuellen Fehlers zurück.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Error. Language-Eigenschaft (Mergemod. h)
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
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368614"
---
# <a name="errorlanguage-property"></a>Error. Language (Eigenschaft)

Die schreibgeschützte **Language** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt die **LangID** des aktuellen Fehlers zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Wert der **Language** -Eigenschaft ist-1, es sei denn, der Fehler ist vom Typ msmerrorlanguageunsupported oder msmerrorlanguagefailed. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

