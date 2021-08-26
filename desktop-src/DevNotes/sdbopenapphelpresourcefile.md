---
description: Lädt die Apphelp-Ressourcendatei.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044990"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile-Funktion

Lädt die Apphelp-Ressourcendatei.

## <a name="syntax"></a>Syntax


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszACResourceFile* \[ in, optional\]
</dt> <dd>

Der Pfad zur Ressourcendatei. Wenn dieser Parameter **NULL ist,** wird die lokale Ressourcen-DLL geöffnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt ein Handle für die geöffnete Ressourcendatei zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




