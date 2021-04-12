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
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522952"
---
# <a name="path_type-enumeration"></a>Pfadtyp- \_ Enumeration

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

<span id="DOS_PATH"></span><span id="dos_path"></span>**DOS- \_ Pfad**
</dt> <dd>

Standard Pfad.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**NT- \_ Pfad**
</dt> <dd>

Interner Pfad.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbkreatedatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**Sdbopendatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




