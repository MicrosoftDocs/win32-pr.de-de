---
description: Ruft den Index für das angegebene Tag und den Schlüsseltyp aus der angegebenen Datenbank ab.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666475"
---
# <a name="sdbgetindex-function"></a>SdbGetIndex-Funktion

Ruft den Index für das angegebene Tag und den Schlüsseltyp aus der angegebenen Datenbank ab.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tWhich* \[ In\]
</dt> <dd>

Das TAG.

</dd> <dt>

*tKey* \[ In\]
</dt> <dd>

Der Schlüsseltyp.

</dd> <dt>

*lpdwFlags* \[ out, optional\]
</dt> <dd>

Dieser Parameter kann 0 oder **SHIMDB \_ INDEX \_ UNIQUE \_ KEY** (0x00000001) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TAGID** des Indexes oder **TAGID \_ NULL**.

## <a name="remarks"></a>Hinweise

Der resultierende Index kann für Lesevorgänge verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




