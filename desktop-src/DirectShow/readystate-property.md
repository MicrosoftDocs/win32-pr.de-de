---
description: Die "Read-State"-Eigenschaft ruft den "Read ystate" des mswebdvd-Objekts ab.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: "\"Leserystate\"-Eigenschaft (\"ocidl. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366978"
---
# <a name="readystate-property"></a>Eigenschaft "leserystate"

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `ReadyState` Eigenschaft ruft den "Read ystate" des **mswebdvd** -Objekts ab.

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Read-State des Steuer Elements darstellt.



| Rückgabecode | Beschreibung                                               |
|-------------|-----------------------------------------------------------|
| 0           | Standard Initialisierungs Zustand.                             |
| 1           | Das Objekt lädt seine Eigenschaften.                         |
| 2           | Das Objekt wurde initialisiert.                              |
| 3           | Das Objekt ist interaktiv, aber nicht alle Daten sind verfügbar. |
| 4           | Das Objekt hat alle zugehörigen Daten empfangen.                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.

Jedes in eine Webseite eingebettete Objekt macht die- `ReadyState` Eigenschaft verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Ocidl. h"</dt> </dl> |



 

 




