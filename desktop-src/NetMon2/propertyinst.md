---
description: Die PROPERTYINST-Struktur definiert eine Instanz einer Eigenschaft in einem Teil der erkannten Daten. Netzwerkmonitor ordnet eine PROPERTYINST-Struktur zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: PROPERTYINST-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0d1c338fb8b4e63f03bff422e25578132476f70d932e8f17d5b0c39a0f6416e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778500"
---
# <a name="propertyinst-structure"></a>PROPERTYINST-Struktur

Die **PROPERTYINST-Struktur** definiert eine Instanz einer Eigenschaft in einem Teil der erkannten Daten. Netzwerkmonitor ordnet eine **PROPERTYINST-Struktur** zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Member

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

Zeiger auf die [PROPERTYINFO-Struktur,](propertyinfo.md) die die Eigenschaft definiert.

</dd> <dt>

**szPropertyText**
</dt> <dd>

Zeiger auf eine Zeichenfolge, die im Detailbereich der Netzwerkmonitor Ui angezeigt wird.

</dd> <dt>

**lpData**
</dt> <dd>

Zeiger auf den Anfang der Daten für die Eigenschaft. Der Parser bestimmt, wo die Eigenschaftsdaten beginnen.

</dd> <dt>

**lpByte**
</dt> <dd>

Zeiger auf die **BYTE-Daten.**

</dd> <dt>

**lpWord**
</dt> <dd>

Zeiger auf die **WORD-Daten.**

</dd> <dt>

**lpDword**
</dt> <dd>

Zeiger auf die **DWORD-Daten.**

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Zeiger auf die [**LARGEINT-Daten.**](largeint.md)

</dd> <dt>

**lpSysTime**
</dt> <dd>

Zeiger auf die [**SYSTEMTIME-Daten.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Zeiger auf eine [PROPERTYINSTEX-Struktur.](propertyinstex.md) Der **lpPropertyInstEx-Member** wird nur verwendet, wenn Sie [AttachPropertyInstanceEx](attachpropertyinstanceex.md)aufrufen.

Wenn **lpPropertyInstEx** verwendet wird, müssen Sie den **DataLength-Member** auf 0xFFFF festlegen.

</dd> <dt>

**Datalength**
</dt> <dd>

Datenlänge für diese Instanz der -Eigenschaft. Wenn der **lpPropertyInstEx-Member** auf eine [**PROPERTYINSTEX-Struktur**](propertyinstex.md) zeigt, müssen Sie **DataLength** auf 0xFFFF festlegen.

</dd> <dt>

**Level**
</dt> <dd>

Ebeneninformationen.

</dd> <dt>

**HelpID**
</dt> <dd>

Hilfedateikontextbezeichner.

</dd> <dt>

**IFlags**
</dt> <dd>

Fehlerbedingungsflag.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PROPERTYINST-Struktur** definiert eine Instanz einer angefügten Eigenschaft. Der Parser greift über mehrere Hilfsfunktionen auf die **PROPERTYINST-Struktur** zu. Wenn beispielsweise die [**FormatPropertyInstance-Funktion**](formatpropertyinstance.md) aufgerufen wird, um die Daten einer Eigenschaft zu formatieren, ändert sie den **szPropertyText-Member** der **PROPERTYINST-Struktur.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

