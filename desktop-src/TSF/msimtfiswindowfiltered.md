---
title: MsimtfIsWindowFiltered-Funktion
description: Die MsimtfIsWindowFiltered-Funktion testet, ob das fenster nach AIMM (Active Input Method Manager) gefiltert wird.
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered-Textdienstframework
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476750"
---
# <a name="msimtfiswindowfiltered-function"></a>MsimtfIsWindowFiltered-Funktion

Die **MsimtfIsWindowFiltered-Funktion** testet, ob das fenster nach AIMM (Active Input Method Manager) gefiltert wird.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Ein zu testende Fensterhand handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Wenn dieses Fenster vom Aktiven Eingabemethode-Manager gefiltert wird.<br/>     |
| <dl> <dt>**FALSE**</dt> </dl> | Wenn dieses Fenster nicht vom Aktiven Eingabemethode-Manager gefiltert wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein Fenster kann nach IActiveIMMApp::FilterClientWindows gefiltert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





