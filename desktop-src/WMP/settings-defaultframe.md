---
title: Settings. defaultframe
description: Die defaultframe-Eigenschaft gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem ScriptCommand-Ereignis empfangen wird.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultframe-Fenster Media Player
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
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369695"
---
# <a name="settingsdefaultframe"></a>Settings. defaultframe

Die **defaultframe** -Eigenschaft gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand** -Ereignis empfangen wird.

## <a name="syntax"></a>Syntax

Player. Settings. defaultframe

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzeichenfolge, die dem Wert des **Name** -Attributs des Target Frame-Elements entspricht. 

## <a name="remarks"></a>Bemerkungen

Wenn ein Zielframe im **ScriptCommand** -Ereignis selbst angegeben wird, wird diese Eigenschaft ignoriert.

Diese Eigenschaft wird ignoriert, wenn das Applet "Netscape Navigator Java" verwendet wird. Im Navigator zeigt jeder empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an, unabhängig vom Wert der *Einstellungen*. **defaultframe**.

**Windows Media Player 10 Mobile**: Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player. ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Verwenden von Windows Media Player mit Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





