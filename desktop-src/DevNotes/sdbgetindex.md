---
description: Ruft den Index für das angegebene Tag und den angegebenen Schlüsseltyp aus der angegebenen Datenbank ab.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Sdbgetindex-Funktion
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
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483230"
---
# <a name="sdbgetindex-function"></a>Sdbgetindex-Funktion

Ruft den Index für das angegebene Tag und den angegebenen Schlüsseltyp aus der angegebenen Datenbank ab.

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*TDas* \[ in\]
</dt> <dd>

Das-Tag.

</dd> <dt>

*TKey* \[ in\]
</dt> <dd>

Der Schlüsseltyp.

</dd> <dt>

*lpdwflags* \[ Out, optional\]
</dt> <dd>

Dieser Parameter kann 0 oder ein eindeutiger **shimdb- \_ Index \_ \_ Schlüssel** (0x00000001) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** des Indexes oder der **TagID \_ null**.

## <a name="remarks"></a>Bemerkungen

Der resultierende Index kann für Lesevorgänge verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




