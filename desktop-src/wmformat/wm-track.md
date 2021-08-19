---
title: WM/Track
description: Das WM/Track-Attribut enthält die Tracknummer des Inhalts. Dieses Attribut ist nullbasiert und wird aus Gründen der Abwärtskompatibilität unterstützt. Für neue Inhalte sollte stattdessen das WM/TrackNumber-Attribut verwendet werden.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026938"
---
# <a name="wmtrack"></a>WM/Track

Das **WM/Track-Attribut** enthält die Tracknummer des Inhalts. Dieses Attribut ist nullbasiert und wird aus Gründen der Abwärtskompatibilität unterstützt. Für neue Inhalte sollte stattdessen das [**WM/TrackNumber-Attribut**](wm-tracknumber.md) verwendet werden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMTrack

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Viele vorhandene Anwendungen schreiben den Wert für **WM/Track** als **DWORD.** Wenn Sie eine Anwendung erstellen, die Dateien aus unbekannten Quellen abspielt, sollten Sie Code zum Verarbeiten von Zeichenfolgen- und **DWORD-Werten** einschließen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




