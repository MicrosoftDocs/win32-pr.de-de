---
description: In Windows Installer-Versionen 1.0 und 1.1 ist die Path-Eigenschaft immer die leere Zeichenfolge. In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zu der Datei oder dem Verzeichnis zurückzugeben, die nicht erstellt werden konnte.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Error.Path-Eigenschaft (Mergemod.h)
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
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378151"
---
# <a name="errorpath-property"></a>Error.Path-Eigenschaft

In Windows Installer-Versionen 1.0 und 1.1 ist die Path-Eigenschaft immer die leere Zeichenfolge. In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zu der Datei oder dem Verzeichnis zurückzugeben, die nicht erstellt werden konnte.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Dieser Wert ist nur für Fehler vom Typ msmErrorFileCreate oder msmErrorDirCreate gültig. Sie können den Fehlertyp ermitteln, indem Sie die [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts**](error-object.md) aufrufen.

### <a name="c"></a>C++

Weitere Informationen finden Sie unter Get Path function [**(Get \_ Path-Funktion).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

