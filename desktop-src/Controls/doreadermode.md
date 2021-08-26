---
title: DoReaderMode-Funktion
description: Aktiviert den Readermodus in einem Fenster.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode-Funktion Windows Controls
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63b71538e41e4b70155da8352e531b620fbe5de7f62746713c3a2a58f3adddf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002690"
---
# <a name="doreadermode-function"></a>DoReaderMode-Funktion

\[**DoReaderMode** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar.\]

Aktiviert den Readermodus in einem Fenster.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prmi* \[ In\]
</dt> <dd>

Typ: **PREADERMODEINFO**

Ein Zeiger auf eine [**READERMODEINFO-Struktur,**](readermodeinfo.md) die Initialisierungsinformationen für den Readermodus enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Readermodus wird über unterstützte Geräte per Mausklick aktiviert, in der Regel mit einer dritten Maustaste oder einem Scrollrad. Nachfolgende Mausbewegungen in einem angegebenen Bereich scrollen in den Inhalt dieses Bereichs, anstatt einen Zeiger zu bewegen. Außerhalb dieses Bereichs wird der Mauszeiger angezeigt und funktioniert normal. Ein zweiter Klick auf die Schaltfläche oder das Scrollrad gibt das Gerät aus dem Readermodus frei.

> [!Note]  
> Diese Funktion wird in keinem öffentlichen Header deklariert. Um es zu verwenden, müssen Sie über Comctl32.dll als Ordnungszahl 383 darauf zugreifen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 4.72 oder höher)</dt> </dl> |



 

 





