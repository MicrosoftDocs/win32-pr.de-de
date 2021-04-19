---
description: Die Eigenschaft schreibgeschützte Abhängigkeiten des Merge-Objekts gibt eine Auflistung von Abhängigkeits Objekten zurück, die einen Satz von nicht erfüllten Abhängigkeiten für die aktuelle Datenbank auflistet.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Merge. Abhängigkeiten-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369690"
---
# <a name="mergedependencies-property"></a>Merge. Abhängigkeiten (Eigenschaft)

Die Eigenschaft schreibgeschützte **Abhängigkeiten** des [**Merge**](merge-object.md) -Objekts gibt eine Auflistung von [**Abhängigkeits**](dependency-object.md) Objekten zurück, die einen Satz von nicht erfüllten Abhängigkeiten für die aktuelle Datenbank auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Ein Modul muss nicht geöffnet sein, um Abhängigkeitsinformationen abzurufen.

### <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get- \_ Abhängigkeiten**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
