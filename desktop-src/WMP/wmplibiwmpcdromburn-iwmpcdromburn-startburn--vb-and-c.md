---
title: Iwmpcdromburn-startburn-Methode
description: Die startburn-Methode verbrennt die CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- startburn-Methode (Windows Media Player)
- startburn-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, startburn-Methode
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
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369131"
---
# <a name="iwmpcdromburnstartburn-method"></a>Iwmpcdromburn:: startburn-Methode

Die **startburn** -Methode verbrennt die CD.

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

## <a name="remarks"></a>Bemerkungen

Vor dem Aufruf dieser Methode sollte " **burnstate** " den Wert "wmpbsready" oder "wmpbsbeendet" aufweisen.

Diese Methode funktioniert nicht, wenn das CD-Laufwerk kein Brenner ist, oder wenn die Festplatte im Laufwerk nicht beschreibbar ist. Verwenden Sie **IsAvailable** , um zu bestimmen, ob eine CD gebrannt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromburn. burnstate (VB und c#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromburn. IsAvailable (VB und c#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromburn. stopburn (VB und c#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





