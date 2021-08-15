---
description: Die schreibgeschützte ConfigurableItems-Eigenschaft des Merge-Objekts gibt eine Auflistung von ConfigurableItem-Objekten zurück, von denen jedes eine einzelne Zeile aus der ModuleConfiguration-Tabelle darstellt.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.ConfigurableItems-Eigenschaft (Mergemod.h)
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
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013038"
---
# <a name="mergeconfigurableitems-property"></a>Merge.ConfigurableItems-Eigenschaft

Die schreibgeschützte **ConfigurableItems-Eigenschaft** des [**Merge-Objekts**](merge-object.md) gibt eine Auflistung [**von ConfigurableItem-Objekten**](configurableitem-object.md) zurück, von denen jedes eine einzelne Zeile aus der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)darstellt. Semantisch stellt jede Schnittstelle im Enumerator ein Element dar, das vom Modulverbraucher konfiguriert werden kann. Die Auflistung ist eine schreibgeschützte Auflistung und implementiert die standardmäßigen schreibgeschützten Auflistungsschnittstellen von Item(), Count() und \_ NewEnum(). Der **Enumerator IEnumMsmConfigItems** implementiert Next(), Skip(), Reset() und Clone() mit der Standardsemantik.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="c"></a>C++

Siehe [**get \_ ConfigurableItems-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




