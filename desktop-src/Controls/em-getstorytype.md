---
title: EM_GETSTORYTYPE Meldung (RichEdit. h)
description: Ruft den Story-Typ ab.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Windows-Steuerelemente für EM_GETSTORYTYPE Meldung
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858850"
---
# <a name="em_getstorytype-message"></a>EM \_ getstorytype-Meldung

Ruft den Story-Typ ab.


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Story-Index.

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Story-Typ zurück, bei dem es sich um einen vom Client definierten benutzerdefinierten Wert oder einen der folgenden Werte handeln kann:

<dl> <dt>

**[**tomcommentsstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomendnotesstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomevenpgesfooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomevenpagesheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomfindstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomfirstpagefooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomfirstpageheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomfootnotesstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tommaintextstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomprimaryfooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomprimaryheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomreplacestory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomscratchstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomtextframestory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomunknownstory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ setstorytype**](em-setstorytype.md)
</dt> <dt>

[**Itextstoryranges:: Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





