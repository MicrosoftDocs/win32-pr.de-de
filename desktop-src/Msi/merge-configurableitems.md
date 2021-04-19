---
description: Die schreibgeschützte configurableitems-Eigenschaft des Merge-Objekts gibt eine Sammlung configurableitem-Objekte zurück, die jeweils eine einzelne Zeile aus der ModuleConfiguration-Tabelle darstellen.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configurableitems-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359339"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Configurableitems (Eigenschaft)

Die schreibgeschützte **configurableitems** -Eigenschaft des [**Merge**](merge-object.md) -Objekts gibt eine Sammlung [**configurableitem**](configurableitem-object.md) -Objekte zurück, die jeweils eine einzelne Zeile aus der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)darstellen. Semantisch stellt jede Schnittstelle im Enumerator ein Element dar, das vom modulconsumer konfiguriert werden kann. Die-Auflistung ist eine schreibgeschützte Auflistung und implementiert die standardmäßigen schreibgeschützten-Auflistungs Schnittstellen von Item (), count () und \_ netwenum (). Der **ienummsmconfigitems** -Enumerator implementiert Next (), Skip (), Reset () und Clone () mit der Standard Semantik.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="c"></a>C++

Weitere Informationen finden [**Sie unter Get \_ configurableitems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




