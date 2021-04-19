---
description: Die Format-Eigenschaft des configurableitem-Objekts gibt den Wert aus der Spalte Format der Tabelle ModuleConfiguration zurück.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Configurableitem. Format-Eigenschaft (Mergemod. h)
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
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366691"
---
# <a name="configurableitemformat-property"></a>Configurableitem. Format (Eigenschaft)

Die **Format** -Eigenschaft des [**configurableitem**](configurableitem-object.md) -Objekts gibt den Wert aus der Spalte Format der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nur die folgenden Werte aufweisen.



| Konstante                        | Wert |
|---------------------------------|-------|
| **msmconfigurableitemtext**     | 0     |
| **msmconfigurableitemkey**      | 1     |
| **msmconfigurableiteminteger**  | 2     |
| **msmconfigurableitembitfield** | 3     |



 

### <a name="c"></a>C++

Siehe [**get \_ Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




