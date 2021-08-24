---
description: Beginnt den Abschluss der Aufgabe.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: TaskCompletionClient::ApplyTaskCompletion-Methode
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
ms.openlocfilehash: 58c95144077697f1655547a58571ce3475355aa96040ce1815bd3178bc9a1290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773670"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>TaskCompletionClient::ApplyTaskCompletion-Methode

Beginnt den Abschluss der Aufgabe.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptcfCategory* 
</dt> <dd>

Ein -Wert, der die Kategorie der Aufgabe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der einzige unterstützte Wert für *ptcfCategory* ist 0x08000000.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




