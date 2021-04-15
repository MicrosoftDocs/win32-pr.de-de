---
title: WM/Nachverfolgung
description: Das WM/Track-Attribut enthält die Nachverfolgung der Inhalte. Dieses Attribut ist NULL basiert und wird aus Gründen der Abwärtskompatibilität unterstützt. Neuer Inhalt sollte stattdessen das WM/tracknumber-Attribut verwenden.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Nachverfolgen des Windows Media-Formats
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104388900"
---
# <a name="wmtrack"></a>WM/Nachverfolgung

Das **WM/Track-** Attribut enthält die Nachverfolgung der Inhalte. Dieses Attribut ist NULL basiert und wird aus Gründen der Abwärtskompatibilität unterstützt. Neuer Inhalt sollte stattdessen das [**WM/tracknumber-**](wm-tracknumber.md) Attribut verwenden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmtrack

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Viele vorhandene Anwendungen schreiben den Wert für **WM/Track** als **DWORD**. Wenn Sie eine Anwendung erstellen, die Dateien aus unbekannten Quellen wieder gibt, sollten Sie Code einschließen, um sowohl Zeichen folgen-als auch **DWORD** -Werte zu verarbeiten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




