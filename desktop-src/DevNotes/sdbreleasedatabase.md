---
description: Schließt die mit der sdbinitdatabase-Funktion initialisierte Shimdatenbank.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Sdbreleasedatabase-Funktion
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
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523336"
---
# <a name="sdbreleasedatabase-function"></a>Sdbreleasedatabase-Funktion

Schließt die mit der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion initialisierte Shimdatenbank.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsdb* \[ in\]
</dt> <dd>

Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbinitdatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




