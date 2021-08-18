---
title: FONTGROUPHDR-Struktur
description: Enthält die Informationen, die eine Anwendung für den Zugriff auf eine bestimmte Schriftart benötigt. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- FONTGROUPHDR-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51b307b7f5798a57e344096fe46227edf97babbf3547c4c851d71fd8ecdc28da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734478"
---
# <a name="fontgrouphdr-structure"></a>FONTGROUPHDR-Struktur

Enthält die Informationen, die eine Anwendung für den Zugriff auf eine bestimmte Schriftart benötigt. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Member

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der einzelnen Schriftarten, die dieser Ressource zugeordnet sind.

</dd> <dt>

**DE**
</dt> <dd>

Typ: **[ **DIRENTRY**](direntry.md)**

</dd> <dd>

Eine -Struktur, die einen eindeutigen Ordinalbezeichner für jede Schriftart in der Ressource enthält. Der **DE-Member** ist ein Platzhalter für das Array variabler Länge von [**DIRENTRY-Strukturen.**](direntry.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **FONTGROUPHDR-Struktur** folgt den Daten für die einzelnen Schriftarten im . Res-Datei. Der Ressourcencompiler fügt automatisch die **FONTGROUPHDR-Struktur** hinzu, in der Regel als letzten Eintrag in der Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





