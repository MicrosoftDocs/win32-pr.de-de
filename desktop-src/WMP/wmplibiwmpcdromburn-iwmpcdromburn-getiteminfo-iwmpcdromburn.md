---
title: IWMPC untertitelt getItemInfo-Methode
description: Die getItemInfo-Methode ruft den Wert des angegebenen Attributs für die CD ab.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getItemInfo-Windows Media Player
- getItemInfo-Methode Windows Media Player , IWMPC wie Die Schnittstelle
- IWMPC wie die Schnittstellenschnittstelle Windows Media Player , getItemInfo-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cf1a91ad60826e19051a59617157110fbcd8d75eff325f94f9b3f84d759aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116228"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>IWMPCwiedit::getItemInfo-Methode

Die **getItemInfo-Methode** ruft den Wert des angegebenen Attributs für die CD ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItem* \[ In\]
</dt> <dd>

Eine **System.String-Datei,** die einen der folgenden Werte enthält.



| Wert         | Beschreibung                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | Ruft die auf der CD verfügbare Zeit in Sekunden ab.                                          |
| Leer         | Ruft einen **System.Boolean** (dargestellt als Zeichenfolge) ab, der angibt, ob die CD leer ist. |
| FreeSpace     | Ruft den freien Speicherplatz auf der CD in Bytes ab.                                                |
| TotalSpace    | Ruft den Gesamtspeicherplatz auf der CD in Bytes ab.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die der Wert des angegebenen Attributs ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





