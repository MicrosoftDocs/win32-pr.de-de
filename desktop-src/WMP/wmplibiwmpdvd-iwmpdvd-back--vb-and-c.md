---
title: Iwmpdvd-Back-Methode
description: Die Methode "Back" ändert die Anzeige von einem Untermenü in das übergeordnete Menü.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Windows-Media Player der Back-Methode
- Back-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, Back-Methode
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
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358748"
---
# <a name="iwmpdvdback-method"></a>Iwmpdvd:: Back-Methode

Die Methode " **Back** " ändert die Anzeige von einem Untermenü in das übergeordnete Menü.

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

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Einige DVDs werden so erstellt, dass die- `back` Methode über das Root-Menü verfügbar ist, aber wenn Sie aufgerufen wird, wird keine Aktion durchführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





