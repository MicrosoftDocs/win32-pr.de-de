---
title: show urlacl
description: Listet DACLs für die angegebene reservierte URL oder alle reservierten URLs auf.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- urlacl HTTP anzeigen
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f6e2443f4cdb489f8deb6e8b61d3a808e8a0711ce13c8d71edc57001787617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900620"
---
# <a name="show-urlacl"></a>show urlacl

Listet DACLs für die angegebene reservierte URL oder alle reservierten URLs auf.

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_string_
</dt> <dd>

Gibt die vollqualifizierte URL an. Wenn keine Angabe angegeben ist, impliziert alle URLs.

</dd> </dl>

## <a name="examples"></a>Beispiele

**show urlacl url=https://+:80/MyUrl**

**show urlacl url=https://www.contoso.com:80/MyUrl**

 

 




