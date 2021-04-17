---
title: Doreadermode-Funktion
description: Aktiviert den Lesemodus in einem-Fenster.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Windows-Steuerelemente der doreadermode-Funktion
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
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479471"
---
# <a name="doreadermode-function"></a>Doreadermode-Funktion

\[**Doreadermode** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.\]

Aktiviert den Lesemodus in einem-Fenster.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prmi* \[ in\]
</dt> <dd>

Typ: **preadermodeinfo**

Ein Zeiger auf eine [**readermodeinfo**](readermodeinfo.md) -Struktur, die Initialisierungs Informationen für den Lesemodus enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Reader-Modus wird über die unterstützten Geräte per Mausklick aktiviert, in der Regel mit einer dritten Maustaste oder einem Mausrad. Die nachfolgende Mausbewegung in einem angegebenen Bereich führt einen Bildlauf für den Inhalt des Bereichs aus, anstatt einen Zeiger zu verschieben Außerhalb dieses Bereichs wird der Mauszeiger angezeigt und funktioniert normal. Mit einem zweiten Klick auf die Schaltfläche oder das Mausrad wird das Gerät im Lesemodus freigegeben.

> [!Note]  
> Diese Funktion ist in keinem öffentlichen Header deklariert. Um es zu verwenden, müssen Sie über Comctl32.dll als Ordnungszahl 383 darauf zugreifen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 4,72 oder höher)</dt> </dl> |



 

 





