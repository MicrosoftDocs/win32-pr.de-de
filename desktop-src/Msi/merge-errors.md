---
description: Die schreibgeschützte Errors-Eigenschaft des Merge-Objekts gibt eine Auflistung von Error-Objekten zurück, die der aktuelle Fehlersatz ist.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Merge.Errors-Eigenschaft (Mergemod.h)
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
ms.openlocfilehash: 3a6abd02a59582a9fbbc65772d781c93ec68f7ffd29cf165cb624daf7d5c6a3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628908"
---
# <a name="mergeerrors-property"></a>Merge.Errors-Eigenschaft

Die schreibgeschützte **Errors-Eigenschaft** des [**Merge-Objekts**](merge-object.md) gibt eine Auflistung von [**Error-Objekten**](error-object.md) zurück, die der aktuelle Fehlersatz ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Der Abruf ist nicht destruktiv. Mehrere Instanzen der Fehlerauflistung können durch wiederholtes Aufrufen dieser Methode abgerufen werden.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
