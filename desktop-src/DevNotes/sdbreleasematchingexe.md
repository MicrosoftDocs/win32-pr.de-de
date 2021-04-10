---
description: Gibt die von der sdbgetmatchingexe-Funktion verwendeten Ressourcen frei.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Sdbreleasematchingexe-Funktion
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
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041387"
---
# <a name="sdbreleasematchingexe-function"></a>Sdbreleasematchingexe-Funktion

Gibt die von der [**sdbgetmatchingexe**](sdbgetmatchingexe.md) -Funktion verwendeten Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsdb* \[ in\]
</dt> <dd>

Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.

</dd> <dt>

*trexe* \[ in\]
</dt> <dd>

Die von [**sdbgetmatchingexe**](sdbgetmatchingexe.md)zurückgegebene [**tagref**](tagref.md) .

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

[**Sdbgetmatchingexe**](sdbgetmatchingexe.md)
</dt> <dt>

[**Sdbinitdatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




