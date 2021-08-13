---
title: IWMPDVD back-Methode
description: Die back-Methode ändert die Anzeige von einem Untermenü in das übergeordnete Menü.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Back-Windows Media Player
- back-Windows Media Player , IWMPDVD-Schnittstelle
- IWMPDVD-Schnittstelle Windows Media Player , back-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483e8e36f8ac5e539925306a53c04d144fb6de1281878840fc598c96c814f002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414560"
---
# <a name="iwmpdvdback-method"></a>IWMPDVD::back-Methode

Die **back-Methode** ändert die Anzeige von einem Untermenü in das übergeordnete Menü.

## <a name="syntax"></a>Syntax


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jede DVD wird anders verfasst. Einige DVDs werden so verfasst, dass die -Methode über das Stammmenü verfügbar ist, aber wenn sie aufgerufen `back` wird, wird sie nichts tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





