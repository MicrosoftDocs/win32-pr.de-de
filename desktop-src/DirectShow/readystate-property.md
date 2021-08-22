---
description: Die ReadyState-Eigenschaft ruft den ReadyState des MSWebDVD-Objekts ab.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: ReadyState-Eigenschaft (Ocidl.h)
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
ms.openlocfilehash: 029798e66d8ed69dc18bbb23dafc8b047d770f1bc91ac1b86ca7bdb09963c2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072784"
---
# <a name="readystate-property"></a>ReadyState-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `ReadyState` -Eigenschaft ruft den ReadyState des **MSWebDVD-Objekts** ab.

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den ReadyState des Steuerelements darstellt.



| Rückgabecode | Beschreibung                                               |
|-------------|-----------------------------------------------------------|
| 0           | Standardinitialisierungsstatus.                             |
| 1           | Das Objekt lädt seine Eigenschaften.                         |
| 2           | Das Objekt wurde initialisiert.                              |
| 3           | Das Objekt ist interaktiv, aber nicht alle Daten sind verfügbar. |
| 4           | Das Objekt hat alle seine Daten empfangen.                         |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert.

Jedes in eine Webseite eingebettete Objekt macht die `ReadyState` -Eigenschaft verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



 

 




