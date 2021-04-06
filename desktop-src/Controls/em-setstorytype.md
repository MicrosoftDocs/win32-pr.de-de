---
title: EM_SETSTORYTYPE Meldung (RichEdit. h)
description: Legt den Texttyp fest.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Windows-Steuerelemente für EM_SETSTORYTYPE Meldung
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858789"
---
# <a name="em_setstorytype-message"></a>EM \_ setstorytype-Meldung

Legt den Texttyp fest.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Story-Index.

</dd> <dt>

*lParam* 
</dt> <dd>

Der neue Story-Typ. Eine Liste der Story-Typen finden Sie unter [**EM \_ getstorytype**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Texttyp, der festgelegt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





