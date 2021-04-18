---
description: Lädt Farbeinstellungen aus der Registrierung neu.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Frefreshstyle-Funktion
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
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357661"
---
# <a name="frefreshstyle-function"></a>Frefreshstyle-Funktion

Lädt Farbeinstellungen aus der Registrierung neu.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg TRUE zurück. andernfalls false.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist keiner Import Bibliothek oder Header Datei zugeordnet. Es muss mithilfe der [**LoadLibrary**](-loadlibrary.md) -Funktion und der [**GetProcAddress**](-getprocaddress-.md) -Funktion aufgerufen werden.

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

 

 




