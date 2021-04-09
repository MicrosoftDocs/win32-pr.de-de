---
description: Die Manifest-Eigenschaft wird verwendet, um den aktiven Aktivierungs Kontext festzulegen oder zu erhalten.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx. Manifest (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958849"
---
# <a name="actctxmanifest-property"></a>ActCtx. Manifest (Eigenschaft)

Die **Manifest** -Eigenschaft wird verwendet, um den aktiven Aktivierungs Kontext festzulegen oder zu erhalten.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Wenn ein Aktivierungs Kontext mit der angegebenen Manifestressource erstellt werden kann, wird die Manifestressource durch das folgende Skript festgelegt und die durch das Manifest angegebene Aktivierungs Konstante aktiviert. Wenn kein Aktivierungs Kontext aus dem Manifest erstellt werden kann, bleibt der Aktivierungs Kontext auf den aktuell aktiven Aktivierungs Kontext festgelegt.

Actctxobj. Manifest = "<*Manifest-Dateiname*>";

Wenn zuvor ein Aktivierungs Kontext erstellt oder aktiviert wurde, legt das folgende Skript die **Manifest** -Eigenschaft auf den aktuellen Aktivierungs Kontext fest. Wenn zuvor kein Aktivierungs Kontext erstellt oder aktiviert wurde, wird die Eigenschaft **Manifest** auf eine leere Zeichenfolge festgelegt.

"BSTR bstrinmanifest = actctxobj. Manifest"

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.<br/>           |



 

 




