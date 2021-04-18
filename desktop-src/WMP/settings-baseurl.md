---
title: Settings. baseurl
description: Die baseurl-Eigenschaft gibt die Basis-URL für die relative Pfad Auflösung mit URL-Skript Befehlen an, die in Medienelemente eingebettet sind, oder ruft Sie ab.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- "\"Settings. BaseURL\"-Windows-Media Player"
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
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368305"
---
# <a name="settingsbaseurl"></a>Settings. baseurl

Die **baseurl** -Eigenschaft gibt die Basis-URL für die relative Pfad Auflösung mit URL-Skript Befehlen an, die in Medienelemente eingebettet sind, oder ruft Sie ab.

## <a name="syntax"></a>Syntax

Player. Settings. baseurl

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Basis-http-URL an, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird. Die Basis-URL wird wie folgt mit der relative URL verkettet:

1.  Ein nach gestellter Schrägstrich (/) wird dem Wert der **baseurl** -Eigenschaft hinzugefügt.
2.  Ein führender Zeitraum, ein umgekehrter Schrägstrich oder ein Schrägstrich (., \\ , und/) werden aus dem relative URL gelöscht.
3.  Der relative URL wird am Ende der Basis-URL hinzugefügt.
4.  Alle Schrägstriche in der resultierenden voll qualifizierten URL werden in der gleichen Richtung (konvertiert in vorwärts-oder rückwärts Schrägstriche) basierend auf der Richtung des ersten Schrägstrichs in der neuen URL gezeigt.

**Hinweis**

Das Player-Steuerelement unterstützt nicht die Verwendung von zwei Punkten (..) im relative URL, um das übergeordnete Element des aktuellen Speicher Orts anzugeben.

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
</dt> </dl>

 

 





