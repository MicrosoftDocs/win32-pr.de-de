---
title: Einstellungen.defaultFrame
description: Die defaultFrame-Eigenschaft gibt den Namen des Frames an, der zum Anzeigen einer URL verwendet wird, die in einem ScriptCommand-Ereignis empfangen wird, oder ruft diesen ab.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Einstellungen.defaultFrame-Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571810"
---
# <a name="settingsdefaultframe"></a>Einstellungen.defaultFrame

Die **defaultFrame-Eigenschaft** gibt den Namen des Frames an, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand-Ereignis empfangen** wird, oder ruft diesen ab.

## <a name="syntax"></a>Syntax

player.settings.defaultFrame

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit Lese-/Schreibzugriff, die dem Wert des **Name-Attributs** des FRAME-Zielelements entspricht. 

## <a name="remarks"></a>Hinweise

Wenn ein Zielframe im **ScriptCommand-Ereignis** selbst angegeben wird, wird diese Eigenschaft ignoriert.

Diese Eigenschaft wird ignoriert, wenn das Java-Netscape Navigator verwendet wird. Im Navigator zeigt jeder empfangene URL-Skriptbefehl die URL in einem neuen Browserfenster an, unabhängig vom Wert *Einstellungen.* **defaultFrame**.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player.ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> <dt>

[**Verwenden von Windows Media Player mit Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





