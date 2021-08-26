---
description: Ruft das TAG ab, das der angegebenen TAGID zugeordnet ist.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a7e58343cf9a863f6b3cecc7f9b6414414387e2f2b33859de1eb015d65f1a78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058470"
---
# <a name="sdbgettagfromtagid-function"></a>SdbGetTagFromTagID-Funktion

Ruft das TAG ab, das der angegebenen **TAGID** zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tiWhich* \[ In\]
</dt> <dd>

Die **TAGID** für das TAG.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt das TAG zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Etikett**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




