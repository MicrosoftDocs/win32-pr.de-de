---
title: delete cache
description: Leert den gesamten URL-Cache oder löscht Einträge entsprechend der angegebenen URL.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Cache löschen http
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106338235"
---
# <a name="delete-cache"></a>delete cache

Leert den gesamten URL-Cache oder löscht Einträge entsprechend der angegebenen URL.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * Zeichenfolge*
</dt> <dd>

Erforderlich. Gibt die voll qualifizierte URL an.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[rekursiv = \] {Yes \| No}**
</dt> <dd>

Wenn ja, werden alle Einträge unter der angegebenen URL entfernt.

</dd> </dl>

## <a name="examples"></a>Beispiele

**Cache-URL löschen = https://www.contoso.com:80/myresource/ rekursiv = ja**

 

 




