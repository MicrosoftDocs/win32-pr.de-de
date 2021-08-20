---
description: Die Format-Eigenschaft des ConfigurableItem-Objekts gibt den Wert aus der Format -Spalte der ModuleConfiguration-Tabelle zurück.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: ConfigurableItem.Format-Eigenschaft (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ee8770029c8465d1e1a60349010847ff38fdac928bb61cd02b0e5a2b034538c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144004"
---
# <a name="configurableitemformat-property"></a>ConfigurableItem.Format (Eigenschaft)

Die **Format-Eigenschaft** des [**ConfigurableItem-Objekts**](configurableitem-object.md) gibt den Wert aus der Spalte Format der [ModuleConfiguration-Tabelle zurück.](moduleconfiguration-table.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nur die folgenden Werte enthalten.



| Konstante                        | Wert |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

Siehe [**get \_ Format-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




