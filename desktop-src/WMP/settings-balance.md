---
title: Einstellungen.balance
description: Die Balance-Eigenschaft gibt den aktuellen Stereosaldo an oder ruft sie ab.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Einstellungen.balance Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569575"
---
# <a name="settingsbalance"></a>Einstellungen.balance

Die **Balance-Eigenschaft** gibt den aktuellen Stereosaldo an oder ruft sie ab.

## <a name="syntax"></a>Syntax

player.settings.balance

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**long**).  Die Werte liegen zwischen 100 und 100, wobei der Standardwert 0 (null) ist.

## <a name="remarks"></a>Hinweise

Der Wert 0 (null) gibt an, dass das Audio auf dem linken und rechten Kanal auf gleicher Lautstärke wiedergegeben wird. Der Wert 100 gibt an, dass Audio nur im linken Kanal wiedergegeben wird. Der Wert 100 gibt an, dass Audio nur im rechten Kanal wiedergegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> </dl>

 

 





