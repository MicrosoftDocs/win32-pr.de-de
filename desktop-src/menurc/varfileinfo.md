---
title: VarFileInfo-Struktur
description: Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Versionsinformationen, die nicht von einer bestimmten Kombination aus Sprache und Codepage abhängen.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- VarFileInfo-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddae8f913e199e0a1219e5ec36012ba3a3eaf24708ca6771ec075b497107418e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733391"
---
# <a name="varfileinfo-structure"></a>VarFileInfo-Struktur

Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Versionsinformationen, die nicht von einer bestimmten Kombination aus Sprache und Codepage abhängen.

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

**wLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge des gesamten **VarFileInfo-Blocks** in Bytes, einschließlich aller Strukturen, die vom **Children-Element angegeben** werden.

</dd> <dt>

**wValueLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Dieser Member ist immer gleich 0 (null).

</dd> <dt>

**wType**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Datentyp in der Versionsressource. Dieser Member ist 1, wenn die Versionsressource Textdaten enthält, und 0, wenn die Versionsressource Binärdaten enthält.

</dd> <dt>

**szKey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Die Unicode-Zeichenfolge L"VarFileInfo".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

So viele Nullwörter wie erforderlich, um das **Children-Member** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **Var**](var-str.md)**

</dd> <dd>

Enthält in der Regel eine Liste der Sprachen, die von der Anwendung oder DLL unterstützt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist keine echte C-Sprachstruktur, da sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versionsressource erstellt und wird nicht in den Headerdateien angezeigt, die im Lieferumfang des Windows Software Development Kit (SDK) enthalten sind.

Der **Children-Member** der [**VS \_ VERSIONINFO-Struktur**](vs-versioninfo.md) kann null oder eine **VarFileInfo-Struktur** enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





