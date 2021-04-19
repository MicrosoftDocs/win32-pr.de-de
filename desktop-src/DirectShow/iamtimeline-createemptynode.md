---
description: Die Methode "kreateemptynode" erstellt ein neues Zeitachsen Objekt.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Iamtimeline:: erkreateemptynode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370639"
---
# <a name="iamtimelinecreateemptynode-method"></a>Iamtimeline:: erkreateemptynode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `CreateEmptyNode` Methode erstellt ein neues Timeline-Objekt.

Verwenden Sie diese Methode, um Zeitachsen Objekte anstelle der **cokreatanstance** -Funktion zu erstellen, da diese Methode wichtige Initialisierungs Routinen ausführt. Jedes Objekt, das von dieser Methode erstellt wird, unterstützt mindestens die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle sowie andere Schnittstellen, die für diesen Objekttyp spezifisch sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppobj* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des neuen Objekts.

</dd> <dt>

*Type* 
</dt> <dd>

Member des enumerierten Typs der [**Zeitachse \_ \_**](timeline-major-type.md) , der den Typ des zu erstellenden Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Fügen Sie das neue-Objekt nicht zu einer anderen Timeline-Instanz hinzu. Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden.

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




