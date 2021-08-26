---
title: Einstellungen.volume
description: Die Volumeeigenschaft gibt das aktuelle Volume an oder ruft es ab.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Einstellungen.volume Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002210"
---
# <a name="settingsvolume"></a>Einstellungen.volume

Die **Volumeeigenschaft** gibt das aktuelle Volume an oder ruft es ab.

## <a name="syntax"></a>Syntax

player.settings.volume

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**long**), die zwischen 0 und 100 liegt. 

## <a name="remarks"></a>Hinweise

Null gibt kein Volume und 100 das vollständige Volume an. Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte Volumeeinstellung verwendet, die für den Player eingerichtet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> </dl>

 

 





