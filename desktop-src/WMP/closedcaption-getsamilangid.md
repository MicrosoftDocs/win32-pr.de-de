---
title: Closedcaption. getsamilangid-Methode
description: Die getsamilangid-Methode ruft den Gebiets Schema Bezeichner (LCID) einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- getsamilangid-Methode, Windows-Media Player
- getsamilangid-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamilangid-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367160"
---
# <a name="closedcaptiongetsamilangid-method"></a>Closedcaption. getsamilangid-Methode

Die **getsamilangid** -Methode ruft den Gebiets Schema Bezeichner (LCID) einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index der abzurufenden LCID angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück, die die LCID der Sprache mit dem angegebenen Index enthält.

## <a name="remarks"></a>Bemerkungen

Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





