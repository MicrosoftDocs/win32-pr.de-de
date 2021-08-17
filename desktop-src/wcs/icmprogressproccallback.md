---
title: ICMProgressProcCallback-Rückruffunktion
description: Die ICMProgressProcCallback-Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- ICMProgressProcCallback-Rückruffunktion Windows Color System
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d697bb09b4871f6debb1a41a7ecc3e795307ee544ec30bfaf4b5b44ba0328578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671386"
---
# <a name="icmprogressproccallback-callback-function"></a>ICMProgressProcCallback-Rückruffunktion

Die **ICMProgressProcCallback-Funktion** ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulMax* 
</dt> <dd>

Gibt den maximalen Wert des Statusindikators an (wird zum Schätzen des Abschlusses der Bitmapverarbeitung verwendet).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Gibt den aktuellen Wert des Fortschrittsindikators an (wenn er durch den Höchstwert dividiert wird, stellt eine grobe Schätzung des Prozentsatzes der Fertigstellung bereit).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Gibt die Daten an, die von der Anwendung an eine ICM2-Funktion übergeben werden, die sie dann an die Rückruffunktion übergibt. Diese Daten können beispielsweise verwendet werden, um die Bitmap und den Prozess zu identifizieren, über den der Fortschritt gemeldet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, um die Bitmapverarbeitung fortzusetzen. Der Rückgabewert ist **FALSE,** um die Verarbeitung abzubrechen. Wenn die Verarbeitung abgebrochen wird, gibt die aufrufende Funktion 0 (null) zurück, um einen Fehler anzugeben, obwohl ihr Ausgabepuffer teilweise gefüllt sein kann.

## <a name="remarks"></a>Hinweise

Der Name dieser Rückruffunktion wird von der Anwendung bereitgestellt. Eine Reihe von WCS-Funktionen, einschließlich [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) und [**CheckBitmapBits,**](/windows/win32/api/icm/nf-icm-checkbitmapbits)rufen diese Funktion in regelmäßigen Abständen auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Icm.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grundlegende Farbverwaltungskonzepte](basic-color-management-concepts.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
