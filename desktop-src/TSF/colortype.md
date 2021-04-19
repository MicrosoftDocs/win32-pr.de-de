---
title: ColorType-Enumeration (Software-BDC. h)
description: Elemente der ColorType-Enumeration werden verwendet, um Typen von Farben anzugeben, die für eine weiche Tastatur verfügbar sind.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Color Type-Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342860"
---
# <a name="colortype-enumeration"></a>ColorType-Enumeration

Elemente der **ColorType** -Enumeration werden verwendet, um Typen von Farben anzugeben, die für eine weiche Tastatur verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**
</dt> <dd>

Hintergrundfarbe.

</dd> <dt>

<span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**Unselforecolor**
</dt> <dd>

Nicht ausgewählte Vordergrundfarbe.

</dd> <dt>

<span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**Unseltextcolor**
</dt> <dd>

Nicht ausgewählte Textfarbe.

</dd> <dt>

<span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**Selforecolor**
</dt> <dd>

Ausgewählte Vordergrundfarbe.

</dd> <dt>

<span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**Seltextcolor**
</dt> <dd>

Ausgewählte Textfarbe.

</dd> <dt>

<span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max \_ - \_ Farbtyp**
</dt> <dd>

Der maximale Farbtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |



 

 





