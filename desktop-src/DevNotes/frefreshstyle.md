---
description: Lädt Farbeinstellungen erneut aus der Registrierung.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103690"
---
# <a name="frefreshstyle-function"></a>FRefreshStyle-Funktion

Lädt Farbeinstellungen erneut aus der Registrierung.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt TRUE bei Erfolg zurück. andernfalls FALSE.

## <a name="remarks"></a>Hinweise

Diese Funktion ist keiner Importbibliothek oder Headerdatei zugeordnet. Sie muss mithilfe der [**Funktionen LoadLibrary**](-loadlibrary.md) und [**GetProcAddress**](-getprocaddress-.md) aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




