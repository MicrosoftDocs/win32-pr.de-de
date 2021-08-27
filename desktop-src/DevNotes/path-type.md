---
description: Stellt den Typ des Pfads dar, der als Argument verwendet wird.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058600"
---
# <a name="path_type-enumeration"></a>PATH \_ TYPE-Enumeration

Stellt den Typ des Pfads dar, der als Argument verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**\_DOS-PFAD**
</dt> <dd>

Standardpfad.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**NT \_ PATH**
</dt> <dd>

Interner Pfad.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




