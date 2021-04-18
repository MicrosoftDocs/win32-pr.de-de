---
description: Die Eigenschaft Schreib geschützter Fehler des Merge-Objekts gibt eine Auflistung von Fehler Objekten zurück, die den aktuellen Satz von Fehlern ist.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Merge. Errors-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351309"
---
# <a name="mergeerrors-property"></a>Merge. Errors-Eigenschaft

Die Eigenschaft Schreib geschützter **Fehler** des [**Merge**](merge-object.md) -Objekts gibt eine Auflistung von [**Fehler**](error-object.md) Objekten zurück, die den aktuellen Satz von Fehlern ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Abruf ist nicht destruktiv. Mehrere Instanzen der Fehlersammlung können durch wiederholtes Aufrufen dieser Methode abgerufen werden.

### <a name="c"></a>C++

Siehe [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
