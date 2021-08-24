---
title: ClosedCaption.getSAMILangName-Methode
description: Die getSAMILangName-Methode ruft den Namen einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- getSAMILangName-Windows Media Player
- getSAMILangName-Methode Windows Media Player , ClosedCaption-Klasse
- ClosedCaption-Klasse Windows Media Player , getSAMILangName-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764030"
---
# <a name="closedcaptiongetsamilangname-method"></a>ClosedCaption.getSAMILangName-Methode

Die **getSAMILangName-Methode** ruft den Namen einer Sprache ab, die von der aktuellen SAMI-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** **(long)** gibt den Index des abzurufenden Sprachnamens an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge zurück,** die den Namen der Sprache enthält, wie in der SAMI-Datei angegeben.

## <a name="remarks"></a>Hinweise

Die Sprachen in einer SAMI-Datei werden in der Reihenfolge indiziert, die in der Datei angezeigt wird, beginnend mit 0 (null).

Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei geöffnet ist (*Player*.**openState** ist gleich 13).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





