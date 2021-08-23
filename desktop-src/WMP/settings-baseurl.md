---
title: Einstellungen.baseURL
description: Die baseURL-Eigenschaft gibt die Basis-URL an, die für die relative Pfadauflösung mit URL-Skriptbefehlen verwendet wird, die in Medienelemente eingebettet sind, oder ruft sie ab.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Einstellungen.baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e06275a3028df6b90d25665e11aab3c2a0961dfa6c525cde0636434f06986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995380"
---
# <a name="settingsbaseurl"></a>Einstellungen.baseURL

Die **baseURL-Eigenschaft** gibt die Basis-URL an, die für die relative Pfadauflösung mit URL-Skriptbefehlen verwendet wird, die in Medienelemente eingebettet sind, oder ruft sie ab.

## <a name="syntax"></a>Syntax

player.settings.baseURL

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die HTTP-Basis-URL an, die vom **ScriptCommand-Ereignis** als Befehlsparameter übergeben wird. Die Basis-URL wird wie folgt mit relative URL verkettet:

1.  Dem Wert der **baseURL-Eigenschaft** wird ein nachgeschlagener Schrägstrich (/) hinzugefügt.
2.  Ein führender Zeitraum, rückwärts gerichteter Schrägstrich oder Schrägstrich (., und /) werden aus \\ der relative URL.
3.  Die relative URL wird am Ende der Basis-URL hinzugefügt.
4.  Alle Schrägstriche in der resultierenden vollqualifizierten URL werden in derselben Richtung angezeigt (konvertiert in Schrägstriche oder Rückwärtsstriche), basierend auf der Richtung des ersten Schrägstrichs, der in der neuen URL gefunden wird.

**Hinweis**

Das Player-Steuerelement unterstützt nicht die Verwendung von zwei Zeiträumen (..) in der relative URL, um das übergeordnete Element der aktuellen Position anzugeben.

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
</dt> </dl>

 

 





