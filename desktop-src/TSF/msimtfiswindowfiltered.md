---
title: Msimtfiswindowgefilterte-Funktion
description: Die Funktion "msimtfiswindowgefiltertert" testet, ob das angegebene Fenster von "AIMM" gefiltert wird (aktiver Eingabemethoden-Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Msimtfiswindowgefiltertes Funktions Text Dienst-Framework
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
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105398"
---
# <a name="msimtfiswindowfiltered-function"></a>Msimtfiswindowgefilterte-Funktion

Die Funktion " **msimtfiswindowgefiltertert** " testet, ob das angegebene Fenster von "AIMM" gefiltert wird (aktiver Eingabemethoden-Manager).

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Fenster Handle, das getestet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | , Wenn dieses Fenster vom aktiven Eingabemethoden-Manager gefiltert wird.<br/>     |
| <dl> <dt>**Alarm**</dt> </dl> | , Wenn dieses Fenster nicht vom aktiven Eingabemethoden-Manager gefiltert wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Fenster kann von iactiveimmapp:: filterclientwindows gefiltert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





