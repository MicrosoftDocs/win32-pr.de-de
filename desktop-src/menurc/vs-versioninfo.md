---
title: VS_VERSIONINFO Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Dabei handelt es sich um die Stamm Struktur, die alle anderen Datei Versions Informationsstrukturen enthält.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106161"
---
# <a name="vs_versioninfo-structure"></a>VS \_ VERSIONINFO-Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Dabei handelt es sich um die Stamm Struktur, die alle anderen Datei Versions Informationsstrukturen enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge der **vs \_ VERSIONINFO** -Struktur in Bytes. Diese Länge schließt keine Auffüll Zeichen ein, die nachfolgende Versions Ressourcen Daten an einer 32-Bit-Grenze ausrichten.

</dd> <dt>

**wvaluelength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge (in Byte) des **Wertmembers** . Dieser Wert ist 0 (null), wenn der aktuellen Versions Struktur kein **Wert** Element zugeordnet ist.

</dd> <dt>

**wType**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Typ der Daten in der Versions Ressource. Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.

</dd> <dt>

**szkey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Die Unicode-Zeichenfolge L "vs- \_ Versions \_ Informationen".

</dd> <dt>

**Padding1**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Enthält so viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **[ **vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Beliebige Daten, die dieser **vs \_ VERSIONINFO** -Struktur zugeordnet sind. Der **wvaluelength** -Member gibt die Länge dieses Members an. Wenn **wvaluelength** gleich 0 (null) ist, ist dieser Member nicht vorhanden.

</dd> <dt>

**Padding2**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten. Diese Bytes sind nicht in **wvaluelength** enthalten. Dieses Member ist optional.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein Array von 0 (null) oder einer [**stringfileinfo**](stringfileinfo.md) -Struktur und NULL oder eine [**varfileinfo**](varfileinfo.md) -Struktur, die untergeordnete Elemente der aktuellen **vs \_ VERSIONINFO** -Struktur sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Stringfileingefo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**Varfileingefo**](varfileinfo.md)
</dt> <dt>

[**VS \_ fixedfileingefo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





