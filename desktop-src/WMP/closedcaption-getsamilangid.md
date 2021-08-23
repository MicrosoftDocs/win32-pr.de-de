---
title: ClosedCaption.getSAMILangID-Methode
description: Die getSAMILangID-Methode ruft den Locale Identifier (LCID) einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- getSAMILangID-Windows Media Player
- getSAMILangID-Methode Windows Media Player , ClosedCaption-Klasse
- ClosedCaption-Klasse Windows Media Player , getSAMILangID-Methode
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
ms.openlocfilehash: 7317bff13b0dcf29157e4a31c1b854fff781d93460633b64485670fab64e6f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764040"
---
# <a name="closedcaptiongetsamilangid-method"></a>ClosedCaption.getSAMILangID-Methode

Die **getSAMILangID-Methode** ruft den Locale Identifier (LCID) einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index der abzurufenden LCID an gibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück, die die LCID der Sprache mit dem angegebenen Index enthält.

## <a name="remarks"></a>Hinweise

Die Sprachen in einer SAMI-Datei werden in der Reihenfolge indiziert, die in der Datei angezeigt wird, beginnend mit 0 (null).

Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei geöffnet ist (*Player*.**openState** ist gleich 13).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





