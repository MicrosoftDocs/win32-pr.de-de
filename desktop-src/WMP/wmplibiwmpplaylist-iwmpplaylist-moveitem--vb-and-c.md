---
title: Iwmpwiedergabe-Methode "muveitem"
description: Die Methode "muveitem" ändert den Speicherort eines Medien Elements in der Wiedergabeliste.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Windows-Media Player für die Windows-
- muveitem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Methode "muveitem"
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362039"
---
# <a name="iwmpplaylistmoveitem-method"></a>Iwmpwiedergabe:: muveitem-Methode

Die Methode " **muveitem** " ändert den Speicherort eines Medien Elements in der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lindexold* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der ursprüngliche Index ist.

</dd> <dt>

*lindexnew* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der neue Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Elemente nach dem eingefügten Element werden die Indexnummern um 1 erhöhen.

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





