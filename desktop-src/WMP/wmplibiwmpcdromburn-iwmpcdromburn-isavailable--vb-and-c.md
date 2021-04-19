---
title: Iwmpcdromburn IsAvailable-Methode
description: Die IsAvailable-Methode stellt Informationen über das CD-Laufwerk und die Medien bereit.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- IsAvailable-Methode, Windows-Media Player
- IsAvailable-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, IsAvailable-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373831"
---
# <a name="iwmpcdromburnisavailable-method"></a>Iwmpcdromburn:: IsAvailable-Methode

Die **IsAvailable** -Methode stellt Informationen über das CD-Laufwerk und die Medien bereit.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritem* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG                 |
|-------|-----------------------------|
| Brenn  | Das Laufwerk ist ein CD-Brenner.   |
| Discs  | Das Laufwerk enthält eine CD. |
| Löschen | Die CD kann gelöscht werden.       |
| Schreiben | Die CD kann in geschrieben werden.   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Boolean** -Wert, der das Ergebnis angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





