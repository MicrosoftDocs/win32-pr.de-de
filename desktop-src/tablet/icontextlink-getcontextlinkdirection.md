---
description: Ruft den Typ der Beziehung ab, die von IContextLink dargestellt wird.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: IContextLink::GetContextLinkDirection-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 96506836e89f4bb2f8b202373df09b5cc6ee1c7f6e9e01f3b68bb2bbe2c8b56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057910"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a>IContextLink::GetContextLinkDirection-Methode

Ruft den Typ der Beziehung ab, die von [**IContextLink**](icontextlink.md) dargestellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContextLinkDirection* \[ out\]
</dt> <dd>

Die Richtung, die [**dieser IContextLink**](icontextlink.md) darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




