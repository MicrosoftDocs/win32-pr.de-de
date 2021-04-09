---
description: Erstellt einen Schlüssel aus einer Zeichenfolge.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Sdbmakeindexkeyfromstring-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958119"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Sdbmakeindexkeyfromstring-Funktion

Erstellt einen Schlüssel aus einer Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszkey* \[ in\]
</dt> <dd>

Die Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt den Schlüssel zurück, oder 0, wenn ein Fehler vorliegt.

## <a name="remarks"></a>Bemerkungen

Der Standard Index Schlüssel ist die ersten acht Zeichen der Zeichenfolge, die in Großbuchstaben konvertiert und dann in einen **ULONGLONG** -Wert umgewandelt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




