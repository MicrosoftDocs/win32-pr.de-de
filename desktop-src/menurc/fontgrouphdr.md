---
title: Fontgrouphdr-Struktur
description: Enthält die Informationen, die für eine Anwendung erforderlich sind, um auf eine bestimmte Schriftart zuzugreifen. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Fontgrouphdr-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213734"
---
# <a name="fontgrouphdr-structure"></a>Fontgrouphdr-Struktur

Enthält die Informationen, die für eine Anwendung erforderlich sind, um auf eine bestimmte Schriftart zuzugreifen. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Member

<dl> <dt>

**Numoffonts**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der einzelnen Schriftarten, die dieser Ressource zugeordnet sind.

</dd> <dt>

**DE**
</dt> <dd>

Typ: **[ **direntry**](direntry.md)**

</dd> <dd>

Eine-Struktur, die einen eindeutigen ordinalbezeichner für jede Schriftart in der Ressource enthält. Der Member " **de** " ist ein Platzhalter für das Array mit [**direntry**](direntry.md) -Strukturen variabler Länge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **fontgrouphdr** -Struktur folgt den Daten für die einzelnen Schriftarten in. Res-Datei. Der Ressourcen Compiler fügt die **fontgrouphdr** -Struktur in der Regel automatisch als letzten Eintrag in der Datei hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Direntry**](direntry.md)
</dt> <dt>

[**Fontdirentry**](fontdirentry.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





