---
description: Sucht nach der angegebenen ausführbaren Datei.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Sdbgetmatchingexe-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861051"
---
# <a name="sdbgetmatchingexe-function"></a>Sdbgetmatchingexe-Funktion

Sucht nach der angegebenen ausführbaren Datei.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsdb* \[ in, optional\]
</dt> <dd>

Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.

</dd> <dt>

*szpath* \[ in\]
</dt> <dd>

Der Pfad der ausführbaren Datei.

</dd> <dt>

*szModuleName* \[ in, optional\]
</dt> <dd>

Der Modulname.

</dd> <dt>

*pszenvironment* \[ in, optional\]
</dt> <dd>

Die Umgebungsvariablen, die als Such Kontext verwendet werden sollen.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter kann 0 oder **sdbgmef \_ Ignore \_ Environment** (0x1) sein.

</dd> <dt>

*pqueryresult* \[ vorgenommen\]
</dt> <dd>

Eine [**sdbqueryresult**](sdbqueryresult.md) -Struktur. Wenn keine Entsprechung gefunden wird, enthält die Struktur **tagref \_ null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die zurückgegebene [**tagref**](tagref.md)abgeschlossen haben, können Sie Sie mit der [**sdbreleasematchingexe**](sdbreleasematchingexe.md) -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbinitdatabase**](sdbinitdatabase.md)
</dt> <dt>

[**Sdbreleasematchingexe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




