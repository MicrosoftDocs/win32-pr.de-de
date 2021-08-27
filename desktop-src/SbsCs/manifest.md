---
description: Die Manifest-Eigenschaft wird verwendet, um den aktiven Aktivierungskontext festzulegen oder abzurufen.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx.Manifest-Eigenschaft
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
ms.openlocfilehash: 77d45bd0dc97ed99ee976da4e262ed3d4819b0ec4c744a4e0a8d76b98f5bacd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977230"
---
# <a name="actctxmanifest-property"></a>ActCtx.Manifest-Eigenschaft

Die **Manifest-Eigenschaft** wird verwendet, um den aktiven Aktivierungskontext festzulegen oder abzurufen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn ein Aktivierungskontext mit der bereitgestellten Manifestdatei erstellt werden kann, legt das folgende Skript die Manifest-Eigenschaft fest und aktiviert die vom Manifest angegebene Aktivierungskonstante. Wenn ein Aktivierungskontext nicht über das Manifest erstellt werden kann, bleibt der Aktivierungskontext auf den derzeit aktiven Aktivierungskontext festgelegt.

ActCtxObj.Manifest = "<*Manifestdateiname*>";

Wenn zuvor ein Aktivierungskontext erstellt oder aktiviert wurde, legt das folgende Skript die **Manifest-Eigenschaft** auf den aktuellen Aktivierungskontext fest. Wenn zuvor kein Aktivierungskontext erstellt oder aktiviert wurde, wird die **Manifest-Eigenschaft** auf eine leere Zeichenfolge festgelegt.

"BSTR bstrManifest = ActCtxObj.Manifest"

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx ist als 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28 definiert.<br/>           |



 

 




