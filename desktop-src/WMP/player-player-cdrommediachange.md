---
title: Player. cdrommediachange-Ereignis
description: Das cdrommediachange-Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird. | Player. cdrommediachange-Ereignis
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Cdrommediachange-Ereignisfenster Media Player
- Cdrommediachange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, cdrommediachange-Ereignis
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
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364664"
---
# <a name="playercdrommediachange-event"></a>Player. cdrommediachange-Ereignis

Das **cdrommediachange** -Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cdromnum* 
</dt> <dd>

**Zahl** (**Long**), die den Index des CD-oder DVD-Laufwerks angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Index des CD-Laufwerks entspricht dem Index eines **CDROM** -Objekts in der **cdromcollection**.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Cdromcollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





