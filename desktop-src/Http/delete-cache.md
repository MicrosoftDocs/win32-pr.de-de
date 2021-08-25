---
title: delete cache
description: Leert den gesamten URL-Cache oder löscht Einträge gemäß der angegebenen URL.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- DELETE CACHE HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c41f2147f0101f312a7fa76796032ec8c821fcea9c08cf89bb3174ddace43d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870560"
---
# <a name="delete-cache"></a>delete cache

Leert den gesamten URL-Cache oder löscht Einträge gemäß der angegebenen URL.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_string_
</dt> <dd>

Erforderlich. Gibt die vollqualifizierte URL an.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive= \] {yes \| no}**
</dt> <dd>

Wenn ja, werden alle Einträge unter der angegebenen URL entfernt.

</dd> </dl>

## <a name="examples"></a>Beispiele

**delete cache url= https://www.contoso.com:80/myresource/ recursive=yes**

 

 




