---
title: Player. domainchange-Ereignis
description: Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird. | Player. domainchange-Ereignis
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Windows-Media Player für Domänen Änderungs Ereignisse
- Domainchange-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, domainchange-Ereignis
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
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365487"
---
# <a name="playerdomainchange-event"></a>Player. domainchange-Ereignis

Das **domainchange** -Ereignis tritt auf, wenn die DVD-Domäne geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Domäne* 
</dt> <dd>

**Zeichenfolge** , die die neue Domäne angibt. Enthält einen der folgenden Werte.



| Zeichenfolge            | Beschreibung                                                          |
|-------------------|----------------------------------------------------------------------|
| FirstPlay         | Die Standard Initialisierung einer DVD-CD wird durchgeführt.                     |
| videomanagermenu  | Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "Root Menu" oder "topmenu" bezeichnet. |
| videotitlesetmenu | Anzeigen von Menüs für den aktuellen Titel Satz. Wird auch als titlemenu bezeichnet.     |
| title             | Anzeigen des aktuellen Titels.                                        |
| stop              | Der DVD-Navigator befindet sich in der DVD-stoppdomäne.                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





