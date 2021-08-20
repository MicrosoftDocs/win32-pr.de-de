---
title: IWMPC erase Erase-Methode
description: Die erase-Methode löscht die aktuelle CD.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- erase-Methode Windows Media Player
- erase-Methode Windows Media Player , IWMPCnutzeroberfläche
- IWMPCnutzeroberfläche Windows Media Player , erase-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356b7bcdd332198c40760860e69741e76e0e993b6b47b3c5a5ff207d3d55bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116333"
---
# <a name="iwmpcdromburnerase-method"></a>IWMPCakuSer::erase-Methode

Die **erase-Methode** löscht die aktuelle CD.

## <a name="syntax"></a>Syntax


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode funktioniert nicht, wenn der Datenträger auf dem Laufwerk nicht neu geschrieben werden kann. Bestimmen Sie mithilfe von [IWMPC csv Ausfüge.isAvailable,](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) ob eine CD gelöscht werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





