---
description: Mit der Methode "-Methode" des Microsoft. Windows. ActCtx-Objekts wird ein Objekt im Kontext des aktuellen Manifests erstellt.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. kreateobject-Methode
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
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216545"
---
# <a name="actctxcreateobject-method"></a>ActCtx. kreateobject-Methode

Mit **der Methode "** -Methode" des [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) -Objekts wird ein Objekt im Kontext des aktuellen Manifests erstellt.

## <a name="syntax"></a>Syntax


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ObjectID* 
</dt> <dd>

Eine Zeichenfolge, die den Typ des zu erstellenden Objekts angibt. Beispielsweise eine COM-ProgID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetObject-Methode**](getobject.md)
</dt> </dl>

 

 




