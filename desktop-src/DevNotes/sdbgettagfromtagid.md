---
description: Ruft das Tag ab, das mit der angegebenen TagID verknüpft ist.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Sdbgettagfromtagid-Funktion
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
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126722"
---
# <a name="sdbgettagfromtagid-function"></a>Sdbgettagfromtagid-Funktion

Ruft das Tag ab, das mit der angegebenen **TagID** verknüpft ist.

## <a name="syntax"></a>Syntax


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiwhat* \[ in\]
</dt> <dd>

Die **TagID** für das Tag.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt das-Tag zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tag**](tag.md)
</dt> <dt>

[**TagID**](tagid.md)
</dt> </dl>

 

 




