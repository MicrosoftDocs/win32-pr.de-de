---
description: Ruft das System-AppPatch-Verzeichnis ab.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Sdbgetapppatchdir-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125635"
---
# <a name="sdbgetapppatchdir-function"></a>Sdbgetapppatchdir-Funktion

Ruft das System-AppPatch-Verzeichnis ab.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsdb* \[ in, optional\]
</dt> <dd>

Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.

</dd> <dt>

*szapppatchpath* \[ vorgenommen\]
</dt> <dd>

Der resultierende Pfad.

</dd> <dt>

*cchsize* \[ in\]
</dt> <dd>

Die Größe des *szapppatchpath* -Puffers in Zeichen. Wenn die Funktion fehlschlägt, wird dieser Parameter auf die leere Zeichenfolge ("") festgelegt.

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

 

 




