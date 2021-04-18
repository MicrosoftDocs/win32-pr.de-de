---
description: Die loadtchar-Funktion wird von Monitoren aufgerufen, um eine Zeichen folgen Variable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurations Zeichenfolge stammt
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Loadtchar-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343706"
---
# <a name="loadtchar-function"></a>Loadtchar-Funktion

Die **loadtchar** -Funktion wird von Monitoren aufgerufen, um eine Zeichen folgen Variable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurations Zeichenfolge stammt

## <a name="syntax"></a>Syntax


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pConfig* \[ in\]
</dt> <dd>

Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.

</dd> <dt>

*pvarname* \[ in\]
</dt> <dd>

Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.

</dd> <dt>

*ppszstring* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeichen folgen Zeiger. Wenn der angeforderte Variablenname gefunden wird, wird die Zeichenfolge zugeordnet und diesem Zeiger zugewiesen. Der Benutzer kann den Arbeitsspeicher, der der Zeichenfolge zugeordnet ist, verantwortungsvoll freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




