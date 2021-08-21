---
description: Die ModuleFiles-Eigenschaft des GetFiles-Objekts gibt alle Primärschlüssel der File-Tabelle für das derzeit geöffnete Modul zurück.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: GetFiles.ModuleFiles-Eigenschaft (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b4b7d498979c94de048e72058df4c8bf87fb8607220efe808554d66deb5d89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635940"
---
# <a name="getfilesmodulefiles-property"></a>GetFiles.ModuleFiles (Eigenschaft)

**Die ModuleFiles-Eigenschaft** des [**GetFiles-Objekts**](getfiles-object.md) gibt alle Primärschlüssel der [File-Tabelle](file-table.md) für das derzeit geöffnete Modul zurück. Die Primärschlüssel werden als Auflistung von Zeichenfolgen zurückgegeben. Das Modul muss durch einen Aufruf der [**OpenModule-Methode**](merge-openmodule.md) des [Merge-Objekts geöffnet werden,](merge-object.md) bevor **ModuleFiles aufruft.**

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Beachten Sie, dass die Reihenfolge der in der Auflistung aufgelisteten Dateien möglicherweise nicht in der gleichen Reihenfolge wie in der Tabelle Datei aufgeführt ist.

Wenn das Modul keine Dateitabelle enthält oder keine Dateien in der jeweiligen Sprache enthält, gibt ModuleFiles eine leere Auflistung von Zeichenfolgen zurück.

### <a name="c"></a>C++

Siehe [**get \_ ModuleFiles-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
