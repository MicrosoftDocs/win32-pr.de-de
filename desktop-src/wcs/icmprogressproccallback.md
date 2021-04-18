---
title: ICMProgressProcCallback-Rückruffunktion
description: Die icmprogressproccallback-Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Icmprogressproccallback-Rückruffunktion Windows Color System
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
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371972"
---
# <a name="icmprogressproccallback-callback-function"></a>ICMProgressProcCallback-Rückruffunktion

Die **icmprogressproccallback** -Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.

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

*ulmax* 
</dt> <dd>

Gibt den maximalen Wert des Fortschritts Zählers an (der zum Schätzen der Vervollständigung der bitmapverarbeitung verwendet wird).

</dd> <dt>

*ulcurrent* 
</dt> <dd>

Gibt den aktuellen Wert des Status Zählers an (Wenn dividiert durch den maximalen Wert ist, wird eine grobe Schätzung des Abschlusses in Prozent angegeben).

</dd> <dt>

*ulcallbackdata* 
</dt> <dd>

Gibt die Daten an, die von der Anwendung an eine ICM2-Funktion weitergegeben werden, die Sie dann an die Rückruffunktion übergibt. Diese Daten können z. b. verwendet werden, um die Bitmap und den Prozess zu identifizieren, über den der Fortschritt berichtet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, um die bitmapverarbeitung fortzusetzen. Der Rückgabewert ist " **false** ", um die Verarbeitung abzubrechen. Wenn die Verarbeitung abgebrochen wird, gibt die aufrufende Funktion NULL zurück, um einen Fehler anzugeben, obwohl der Ausgabepuffer möglicherweise teilweise ausgefüllt ist.

## <a name="remarks"></a>Bemerkungen

Der Name dieser Rückruffunktion wird von der Anwendung bereitgestellt. Eine Reihe von WCS-Funktionen, einschließlich [**translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) und [**checkbitmapbits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), wird diese Funktion in regelmäßigen Abständen aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[**Translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**Checkbitmapbits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
