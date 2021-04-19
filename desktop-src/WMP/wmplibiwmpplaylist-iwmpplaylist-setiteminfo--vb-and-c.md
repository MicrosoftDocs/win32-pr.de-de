---
title: Iwmpwiedergabe-Methode
description: Mit der setiteminfo-Methode wird der Wert eines Attributs der aktuellen Wiedergabeliste festgelegt.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365687"
---
# <a name="iwmpplaylistsetiteminfo-method"></a>Iwmpwiedergabe:: abtiteminfo-Methode

Mit der **setiteminfo** -Methode wird der Wert eines Attributs der aktuellen Wiedergabeliste festgelegt.

## <a name="syntax"></a>Syntax


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attribut Name ist.

</dd> <dt>

*bstrauvalue* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attribut Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.

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

[**Iwmpwiedergabe. getiteminfo (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





