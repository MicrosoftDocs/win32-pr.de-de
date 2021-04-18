---
title: Varfileingefo-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die nicht von einer bestimmten Sprache und Codepage kombiniert werden.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Varfileingefo-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344090"
---
# <a name="varfileinfo-structure"></a>Varfileingefo-Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die nicht von einer bestimmten Sprache und Codepage kombiniert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Member

<dl> <dt>

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge des gesamten **varfileinfo** -Blocks (in Bytes), einschließlich aller Strukturen, die vom **Children** -Member angegeben werden.

</dd> <dt>

**wvaluelength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Dieser Member ist immer gleich 0 (null).

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

Die Unicode-Zeichenfolge L "varfileingefo".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **var**](var-str.md)**

</dd> <dd>

Enthält in der Regel eine Liste der Sprachen, die von der Anwendung oder DLL unterstützt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

Das **unter** geordnete Element der [**vs \_ VERSIONINFO**](vs-versioninfo.md) -Struktur kann NULL oder eine **varfileinfo** -Struktur enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Kreis**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





