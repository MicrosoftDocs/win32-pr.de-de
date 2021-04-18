---
description: Die Modulefiles-Eigenschaft des GetFiles-Objekts gibt alle Primärschlüssel der Dateitabelle für das aktuell geöffnete Modul zurück.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: GetFiles. Modulefiles-Eigenschaft (Mergemod. h)
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
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371533"
---
# <a name="getfilesmodulefiles-property"></a>GetFiles. Modulefiles (Eigenschaft)

Die **Modulefiles** -Eigenschaft des [**GetFiles**](getfiles-object.md) -Objekts gibt alle Primärschlüssel der [Dateitabelle](file-table.md) für das aktuell geöffnete Modul zurück. Die Primärschlüssel werden als eine Auflistung von Zeichen folgen zurückgegeben. Das Modul muss durch einen Aufruf der [**OpenModule**](merge-openmodule.md) -Methode des [Merge-Objekts](merge-object.md) geöffnet werden, bevor **Modulefiles** aufgerufen wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die Reihenfolge der in der Auflistung aufgelisteten Dateien möglicherweise nicht in derselben Reihenfolge wie in der Dateitabelle aufgeführt ist.

Wenn das Modul keine Dateitabelle hat oder keine Dateien in der jeweiligen Sprache enthält, gibt Modulefiles eine leere Auflistung von Zeichen folgen zurück.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ Modulefiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
