---
title: ComHandlerAction.Data (Eigenschaft)
description: Für die Skripterstellung ruft zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Dateneigenschafts-Taskplaner
- Dateneigenschaft Taskplaner , ComHandlerAction-Objekt
- ComHandlerAction-Objekt Taskplaner , Data-Eigenschaft
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
ms.openlocfilehash: 254457941d55d9a6b130ec504563236e60baf7ba1a1d44d5851ed3c712634afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139603"
---
# <a name="comhandleractiondata-property"></a>ComHandlerAction.Data (Eigenschaft)

Für die Skripterstellung ruft zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Argumente, die vom Handler benötigt werden.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML werden die Daten eines COM-Handlers im [**Data-Element**](taskschedulerschema-data-comhandlertype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





