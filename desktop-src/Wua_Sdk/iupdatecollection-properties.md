---
description: Die iupdatecollection-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Iupdatecollection-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348201"
---
# <a name="iupdatecollection-properties"></a>Iupdatecollection-Eigenschaften

Die [**iupdatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                        | BESCHREIBUNG                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle ab, die zum Auflisten der Auflistung verwendet werden kann. |
| [**Countdown**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Ruft die Anzahl der Elemente in der Auflistung ab.                                                                           |
| [**Element**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Ruft eine [**iupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) -Schnittstelle in einer Auflistung ab oder legt Sie fest.                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Ruft einen booleschen Wert ab, der angibt, ob die Update-Auflistung schreibgeschützt ist.                                          |



 

 

 
