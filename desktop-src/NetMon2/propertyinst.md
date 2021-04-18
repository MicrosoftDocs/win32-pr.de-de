---
description: Die propertyinst-Struktur definiert eine Instanz einer Eigenschaft in einem erkannten Datenelement. Netzwerkmonitor ordnet eine propertyinst-Struktur zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Propertyinst-Struktur (Netmon. h)
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
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343846"
---
# <a name="propertyinst-structure"></a>Propertyinst-Struktur

Die **propertyinst** -Struktur definiert eine Instanz einer Eigenschaft in einem erkannten Datenelement. Netzwerkmonitor ordnet eine **propertyinst** -Struktur zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.

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

**lppropertyinfo**
</dt> <dd>

Ein Zeiger auf die [PropertyInfo](propertyinfo.md) -Struktur, die die Eigenschaft definiert.

</dd> <dt>

**szpropertytext**
</dt> <dd>

Zeiger auf eine Zeichenfolge, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt wird.

</dd> <dt>

**lpdata**
</dt> <dd>

Zeiger auf den Anfang der Daten für die Eigenschaft. Der Parser bestimmt, wo die Eigenschaften Daten gestartet werden.

</dd> <dt>

**LPBYTE**
</dt> <dd>

Zeiger auf die **Bytedaten** .

</dd> <dt>

**lpword**
</dt> <dd>

Zeiger auf das **Word** -Daten.

</dd> <dt>

**LPDWORD**
</dt> <dd>

Zeiger auf die **DWORD** -Daten.

</dd> <dt>

**lplargeint**
</dt> <dd>

Zeiger auf die [**largeint**](largeint.md) -Daten.

</dd> <dt>

**lpsystime**
</dt> <dd>

Zeiger auf die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Daten.

</dd> <dt>

**lppropertyinstex**
</dt> <dd>

Zeiger auf eine [propertyinstex](propertyinstex.md) -Struktur. Der **lppropertyinstex** -Member wird nur verwendet, wenn Sie [attachpropertyinstanceex](attachpropertyinstanceex.md)aufrufen.

Wenn " **lppropertyinstex** " verwendet wird, müssen Sie das **DATALENGTH** -Element auf "0xFFFF" festlegen.

</dd> <dt>

**DATALENGTH**
</dt> <dd>

Daten Länge für diese Instanz der-Eigenschaft. Wenn das **lppropertyinstex** -Element auf eine [**propertyinstex**](propertyinstex.md) -Struktur verweist, müssen Sie **DATALENGTH** auf 0xFFFF festlegen.

</dd> <dt>

**Level**
</dt> <dd>

Informationen zur Ebene.

</dd> <dt>

**HelpID**
</dt> <dd>

Kontext Bezeichner der Hilfedatei.

</dd> <dt>

**IFlags**
</dt> <dd>

Fehlerbedingungs-Flag.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **propertyinst** -Struktur definiert eine Instanz einer angefügten-Eigenschaft. Der Parser greift über mehrere Hilfsfunktionen auf die **propertyinst** -Struktur zu. Wenn z. b. die [**formatpropertyinstance**](formatpropertyinstance.md) -Funktion aufgerufen wird, um die Daten einer Eigenschaft zu formatieren, ändert Sie den **szpropertytext** -Member der **propertyinst** -Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Attachpropertyinstance](attachpropertyinstance.md)
</dt> <dt>

[Attachpropertyinstanceex](attachpropertyinstanceex.md)
</dt> </dl>

 

