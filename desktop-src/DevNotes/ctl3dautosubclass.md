---
description: Unterklassen werden automatisch Unterklassen und 3D-Effekte zu allen Dialogfeldern in der Anwendung hinzugefügt.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372237"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass-Funktion

Unterklassen werden automatisch Unterklassen und 3D-Effekte zu allen Dialogfeldern in der Anwendung hinzugefügt.

## <a name="syntax"></a>Syntax


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstapp* 
</dt> <dd>

Ein Handle für die Anwendung, die als Client registriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, es sei denn, eine der folgenden Bedingungen ist vorhanden. in diesem Fall wird **false** zurückgegeben:

-   Ctl3d wird unter Windows, Version 3,0 oder früher, ausgeführt.
-   Ctl3d ist in den Tabellen für die aktuelle Anwendung nicht verfügbar. Ctl3d kann bis zu 32 Anwendungen gleichzeitig bedienen.
-   Ctl3d kann seinen CBT-Hook nicht installieren.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
