---
description: Lädt eine IME-Konfiguration erneut aus der HKCU-Registrierung in japanischer IME.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354785"
---
# <a name="reload_config-function"></a>config-Funktion erneut laden \_

Lädt eine IME-Konfiguration erneut aus der HKCU-Registrierung in japanischer IME.

## <a name="syntax"></a>Syntax


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn in HKCU kein Registrierungs Wert vorhanden ist, schreibt die Funktion zum erneuten **Laden \_** von Daten in die Registrierung.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
