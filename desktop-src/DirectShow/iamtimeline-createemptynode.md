---
description: Die CreateEmptyNode-Methode erstellt ein neues Zeitachsenobjekt.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: IAMTimeline::CreateEmptyNode-Methode (Qedit.h)
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
ms.openlocfilehash: 0f98073c7e3a4be7fa57858440e540769eef50c44fae4ddcaed459146bfc788a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389140"
---
# <a name="iamtimelinecreateemptynode-method"></a>IAMTimeline::CreateEmptyNode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `CreateEmptyNode` -Methode erstellt ein neues Zeitachsenobjekt.

Verwenden Sie diese Methode, um Zeitachsenobjekte anstelle der **CoCreateInstance-Funktion** zu erstellen, da diese Methode wichtige Initialisierungsroutinen ausführt. Jedes von dieser Methode erstellte Objekt unterstützt mindestens die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) sowie andere Schnittstellen, die für diesen Objekttyp spezifisch sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des neuen Objekts.

</dd> <dt>

*Typ* 
</dt> <dd>

Member des enumerierten [**TIMELINE \_ MAJOR \_ TYPE-Typs,**](timeline-major-type.md) der den Typ des zu erstellenden Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Fügen Sie das neue Objekt nicht einer anderen Zeitachseninstanz hinzu. Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden.

Wenn die Methode erfolgreich ist, verfügt die [**zurückgegebene IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




