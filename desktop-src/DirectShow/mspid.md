---
description: Hinweis Diese API ist veraltet. Neue Anwendungen sollten sie nicht verwenden. Der MSPID-Datentyp identifiziert den Zweck eines Medientous.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d274fc4131c0aa4494d610cbe1145ad79b848b5f6280d4ad6a10b298a8b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075750"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Diese API ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

Der **MSPID-Datentyp** identifiziert den Zweck eines Medientous.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Hinweise

**MSPID** ist einfach eine Typedef für GUID. Die folgenden MSPIDs sind definiert.



| Wert               | BESCHREIBUNG           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Primärer Videostream. |
| MSPID \_ PrimaryAudio | Primärer Audiostream. |



 

Der **REFMSPID-Typ** definiert einen Verweis auf eine **MSPID.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mmstream.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Multimediastreamingdatentypen](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




