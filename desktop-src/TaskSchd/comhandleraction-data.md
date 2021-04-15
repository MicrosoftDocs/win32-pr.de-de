---
title: Comhandleraction. Data (Eigenschaft)
description: Ruft bei der Skripterstellung zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Daten Eigenschafts Taskplaner
- Dateneigenschaft Taskplaner, comhandleraction-Objekt
- Comhandleraction-Objekt Taskplaner, Dateneigenschaft
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392148"
---
# <a name="comhandleractiondata-property"></a>Comhandleraction. Data (Eigenschaft)

Ruft bei der Skripterstellung zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Argumente, die vom Handler benötigt werden.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML werden die Daten eines com-Handlers im [**Data**](taskschedulerschema-data-comhandlertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Comhandleraction**](comhandleraction.md)
</dt> </dl>

 

 





