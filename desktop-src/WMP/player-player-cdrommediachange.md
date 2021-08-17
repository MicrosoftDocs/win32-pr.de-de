---
title: Player.C csvMediaChange-Ereignis
description: Das C csvMediaChange-Ereignis tritt auf, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird. | Player.C csvMediaChange-Ereignis
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Windows Media Player des CholeMediaChange-Ereignisses
- CmediaMediaChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , CmediaChange-Ereignis
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747386"
---
# <a name="playercdrommediachange-event"></a>Player.C csvMediaChange-Ereignis

Das **C csvMediaChange-Ereignis** tritt auf, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CredoNum* 
</dt> <dd>

**Zahl** (**long**), die den Index des CD- oder DVD-Laufwerks angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Index des CD-Laufwerks entspricht dem Index eines **Cobjekts** in der **CcollectionCollection**.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Chole-Objekt**](cdrom-object.md)
</dt> <dt>

[**CcollectionCollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





