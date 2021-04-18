---
description: Beachten Sie, dass diese API veraltet ist. Diese sollten von neuen Anwendungen nicht verwendet werden. Der mspid-Datentyp identifiziert den Zweck eines Medien Dampfes.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: Mspid (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365712"
---
# <a name="mspid"></a>Mspid

> [!Note]  
> Diese API ist veraltet. Diese sollten von neuen Anwendungen nicht verwendet werden.

 

Der **mspid-** Datentyp identifiziert den Zweck eines Medien Dampfes.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Bemerkungen

**Mspid** ist einfach eine typedef für GUID. Die folgenden mspids sind definiert.



| Wert               | BESCHREIBUNG           |
|---------------------|-----------------------|
| Mspid \_ primaryvideo | Primärer Videostream. |
| Mspid \_ primaryaudio | Primärer Audiodatenstrom. |



 

Der **refmspid-** Typ definiert einen Verweis auf eine **mspid**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mmstream. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Multimedia-streamingdatentypen](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




