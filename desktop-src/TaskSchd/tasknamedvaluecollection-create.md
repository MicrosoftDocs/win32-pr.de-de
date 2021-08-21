---
title: TaskNamedValueCollection.Create-Methode
description: Für die Skripterstellung erstellt ein Name-Wert-Paar in der Auflistung.
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- Erstellen einer Taskplaner
- Create method Taskplaner , TaskNamedValueCollection object
- TaskNamedValueCollection-Objekt Taskplaner , Create-Methode
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d974eb7fb93d3bb617ce122426b4003a708cbe3ed753ba758fdd5f71ed8bc87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858063"
---
# <a name="tasknamedvaluecollectioncreate-method"></a>TaskNamedValueCollection.Create-Methode

Für die Skripterstellung erstellt ein Name-Wert-Paar in der Auflistung.

## <a name="syntax"></a>Syntax


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Der Name, der einem Wert in einem Name-Wert-Paar zugeordnet ist.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Der Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.

</dd> <dt>

*pair* \[ out\]
</dt> <dd>

Das Name-Wert-Paar, das in der Auflistung erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





