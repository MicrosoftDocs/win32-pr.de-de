---
description: In Windows Installer Versionen 1,0 und 1,1 ist die Path-Eigenschaft immer die leere Zeichenfolge. In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zur Datei oder zum Verzeichnis zurückzugeben, die nicht erstellt werden konnte.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Error. Path-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365997"
---
# <a name="errorpath-property"></a>Error. Path-Eigenschaft

In Windows Installer Versionen 1,0 und 1,1 ist die Path-Eigenschaft immer die leere Zeichenfolge. In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zur Datei oder zum Verzeichnis zurückzugeben, die nicht erstellt werden konnte.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist nur für Fehler vom Typ msmerrorfilecreate oder msmerrordircreate gültig. Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.

### <a name="c"></a>C++

Siehe [**get \_ path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

