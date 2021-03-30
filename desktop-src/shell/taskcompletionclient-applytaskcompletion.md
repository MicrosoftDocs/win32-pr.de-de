---
description: Startet den Abschluss der Aufgabe.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Taskcompletionclient:: applytaskcompletion-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994966"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>Taskcompletionclient:: applytaskcompletion-Methode

Startet den Abschluss der Aufgabe.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptcfcategory* 
</dt> <dd>

Ein-Wert, der die Kategorie der Aufgabe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der einzige unterstützte Wert für *ptcfcategory* ist 0x08000000.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Taskcompletionclient**](taskcompletionclient.md)
</dt> </dl>

 

 




