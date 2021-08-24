---
title: IWMPC über die start Ausweichmethode
description: Die startMethod-Methode lädt die CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- startMethod Windows Media Player
- startMethod Windows Media Player , IWMPCnutzeroberfläche
- IWMPC über die Schnittstelle Windows Media Player , startFace-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7806501a619d6172d9f1ce0715045c822b30326c2b59c268f432708ea13923ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761070"
---
# <a name="iwmpcdromburnstartburn-method"></a>IWMPC über die Methode "IWMPCakuSy"::start Auswendung

Die **startMethod-Methode** lädt die CD.

## <a name="syntax"></a>Syntax


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von **burnstate** sollte wmpbsReady oder wmpbsStopped sein, bevor diese Methode aufgerufen wird.

Diese Methode funktioniert nicht, wenn das CD-Laufwerk kein Burner ist oder wenn der Datenträger auf dem Laufwerk nicht beschreibbar ist. Verwenden Sie **isAvailable,** um zu bestimmen, ob eine CD verbraucht werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPC csvOrpora.burnState (VB und C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**IWMPC csvOrpora.isAvailable (VB und C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPC csvOrpora.stop Auswendung (VB und C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





