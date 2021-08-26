---
description: Gibt ressourcen frei, die von der SdbGetMatchingExe-Funktion verwendet werden.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 710874fc0e57775eb6ad1c9c6681a5b74dc66d133b22ce23d2ac0d27270ef7f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044920"
---
# <a name="sdbreleasematchingexe-function"></a>SdbReleaseMatchingExe-Funktion

Gibt ressourcen frei, die von [**der SdbGetMatchingExe-Funktion verwendet**](sdbgetmatchingexe.md) werden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSDB* \[ In\]
</dt> <dd>

Ein Handle für die shim-Datenbank, die von der [**SdbInitDatabase-Funktion zurückgegeben**](sdbinitdatabase.md) wird.

</dd> <dt>

*trExe* \[ In\]
</dt> <dd>

Die von [**SdbGetMatchingExe zurückgegebene**](sdbgetmatchingexe.md) [**TAGREF.**](tagref.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




