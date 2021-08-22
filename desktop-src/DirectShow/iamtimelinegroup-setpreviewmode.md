---
description: Die SetPreviewMode-Methode legt den Vorschaumodus für die Gruppe fest.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: IAMTimelineGroup::SetPreviewMode-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f4c53372066ec28f3782fe53148eaba99489187c3be9b9ccf73195a7b1e6da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756310"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>IAMTimelineGroup::SetPreviewMode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die SetPreviewMode-Methode legt den Vorschaumodus für die Gruppe fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fPreview* 
</dt> <dd>

Der Vorschaumodus. True gibt an, dass sich die Gruppe im Vorschaumodus befindet. **False** gibt an, dass sich die Gruppe im Erstellungsmodus befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Im Vorschaumodus werden Frames bei langsamen Effekten oder Übergängen gelöscht, um das Video mit den Audiodaten zu synchronisieren. Das Video könnte als Ergebnis geschnitten aussehen. Im Erstellungsmodus wird jeder Frame gerendert. Der Erstellungsmodus eignet sich zum Schreiben von Dateien. Für die Bildschirmvorschau ist das Video möglicherweise nicht mit den Audiodaten synchron.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




