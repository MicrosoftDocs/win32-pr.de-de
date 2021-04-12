---
description: Lädt die AppHelp-Ressourcen Datei.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Sdbopenapphelpresourcefile-Funktion
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
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393077"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Sdbopenapphelpresourcefile-Funktion

Lädt die AppHelp-Ressourcen Datei.

## <a name="syntax"></a>Syntax


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszacresourcefile* \[ in, optional\]
</dt> <dd>

Der Pfad zur Ressourcen Datei. Wenn dieser Parameter **null** ist, wird die lokale Ressourcen-DLL geöffnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein Handle für die geöffnete Ressourcen Datei zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




