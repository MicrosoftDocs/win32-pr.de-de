---
description: Ruft die Komponente Windows Image Acquisition (WIA) 2.0 (Vorschauversion) ab.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: IWiaItem2::GetPreviewComponent-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3ac3705b4be60ce53fee411df1142fb64bbd1c393864b644e260829080be8f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450430"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2::GetPreviewComponent-Methode

Ruft die Komponente Windows Image Acquisition (WIA) 2.0 (Vorschauversion) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*ppWiaPreview* \[ out\]
</dt> <dd>

Typ: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Gibt die Adresse eines Zeigers auf die [**IWiaPreview-Schnittstelle**](-wia-iwiapreview.md) der Vorschaukomponente zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, um einen Zeiger auf die Adresse der WIA 2.0-Vorschaukomponente für jedes [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) in der Objektstruktur eines WIA 2.0-Hardwaregeräts zurückzugeben.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Schnittstellenzeiger aufrufen, die sie über den *ppWiaPreview-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
