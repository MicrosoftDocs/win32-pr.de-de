---
description: Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127253"
---
# <a name="indexid"></a>INDEXID

Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Bemerkungen

Eine **IndexID** kann ein ganzzahliger Wert sein, der den Index darstellt, oder der folgende Wert:

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>IndexID \_ NULL ((IndexID)-1)
</dt> <dd>

Ungültige **IndexID**.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbdeclareingedex**](sdbdeclareindex.md)
</dt> <dt>

[**Sdbstartindizierung**](sdbstartindexing.md)
</dt> <dt>

[**Sdbstopindizierung**](sdbstopindexing.md)
</dt> </dl>

 

 




