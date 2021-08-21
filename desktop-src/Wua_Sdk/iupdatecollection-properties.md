---
description: Die IUpdateCollection-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: IUpdateCollection-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859760"
---
# <a name="iupdatecollection-properties"></a>IUpdateCollection-Eigenschaften

Die [**IUpdateCollection-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) definiert die folgenden Eigenschaften.



| Eigenschaft                                        | BESCHREIBUNG                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) ab, die zum Aufzählen der Auflistung verwendet werden kann. |
| [**Anzahl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Ruft die Anzahl der Elemente in der Auflistung ab.                                                                           |
| [**Element**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Ruft eine [**IUpdate-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) in einer Auflistung ab oder legt diese fest.                                                    |
| [**Readonly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Ruft einen booleschen Wert ab, der angibt, ob die Updateauflistung schreibgeschützt ist.                                          |



 

 

 
