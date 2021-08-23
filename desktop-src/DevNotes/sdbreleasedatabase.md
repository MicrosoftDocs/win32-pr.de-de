---
description: Schließt die shim-Datenbank, die mit der SdbInitDatabase-Funktion initialisiert wurde.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 82a7cf785927a5ef14e3e033c29233afcc4a49cf89d610757d110583bce4eff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815330"
---
# <a name="sdbreleasedatabase-function"></a>SdbReleaseDatabase-Funktion

Schließt die shim-Datenbank, die mit der [**SdbInitDatabase-Funktion**](sdbinitdatabase.md) initialisiert wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSDB* \[ In\]
</dt> <dd>

Ein Handle für die shim-Datenbank, die von der [**SdbInitDatabase-Funktion**](sdbinitdatabase.md) zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




