---
description: Lädt eine IME-Konfiguration nur in japanischer IME aus der HKCU-Registrierung neu.
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
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571620"
---
# <a name="reload_config-function"></a>config-Funktion neu laden \_

Lädt eine IME-Konfiguration nur in japanischer IME aus der HKCU-Registrierung neu.

## <a name="syntax"></a>Syntax


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich ist. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn in HKCU kein Registrierungswert vorhanden ist, schreibt die **\_ Neuladekonfigurationsfunktion** erste Daten in die Registrierung.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
