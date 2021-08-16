---
title: Player.DomainChange-Ereignis
description: Das DomainChange-Ereignis tritt auf, wenn sich die DVD-Domäne ändert. | Player.DomainChange-Ereignis
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- DomainChange-Ereignis Windows Media Player
- DomainChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , DomainChange-Ereignis
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d70c6a3c2ac2d29c03e6d0518b5e7341f988f41e1bf2f5bb84a7de9f83f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995910"
---
# <a name="playerdomainchange-event"></a>Player.DomainChange-Ereignis

Das **DomainChange-Ereignis** tritt auf, wenn sich die DVD-Domäne ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strDomain* 
</dt> <dd>

**Zeichenfolge,** die die neue Domäne angibt. Enthält einen der folgenden Werte.



| Zeichenfolge            | Beschreibung                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | Ausführen der Standardinitialisierung eines DVD-Datenträgers.                     |
| videoManagerMenu  | Anzeigen von Menüs für ganze Datenträger. Wird auch als Stammmenü oder topMenu bezeichnet. |
| videoTitleSetMenu | Anzeigen von Menüs für den aktuellen Titelsatz. Wird auch als titleMenu bezeichnet.     |
| title             | Anzeigen des aktuellen Titels.                                        |
| stop              | Der DVD-Navigator befindet sich in der Domäne DVD-Beenden.                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





