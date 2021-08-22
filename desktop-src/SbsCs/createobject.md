---
description: Die CreateObject-Methode von Microsoft. Windows. Das ActCtx-Objekt erstellt ein -Objekt im Kontext des aktuellen Manifests.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx.CreateObject-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 4161ccdcc2562405123d8cb5276aa1f849121c0271b6c6e3f23a32551f6f3dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142393"
---
# <a name="actctxcreateobject-method"></a>ActCtx.CreateObject-Methode

Die **CreateObject-Methode** der [**Microsoft.Windows. Das ActCtx-Objekt**](microsoft-windows-actctx-object.md) erstellt ein -Objekt im Kontext des aktuellen Manifests.

## <a name="syntax"></a>Syntax


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Objectid* 
</dt> <dd>

Eine Zeichenfolge, die den Typ des zu erstellenden Objekts angibt. Beispielsweise eine COM-ProgID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx ist als 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetObject-Methode**](getobject.md)
</dt> </dl>

 

 




