---
description: Initialisiert den Filter. Wird von Windows Image Acquisition (WIA) 2.0 vor jedem Imagedownload aufgerufen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: IWiaImageFilter::InitializeFilter-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 43b818c3adc9926c4ba27f11f5d489ffc0b97e4443d0427e7a12067e9062072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440445"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter::InitializeFilter-Methode

Initialisiert den Filter. Wird von Windows Image Acquisition (WIA) 2.0 vor jedem Imagedownload aufgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWiaItem2* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Gibt einen Zeiger auf das [**IWiaItem2-Element**](-wia-iwiaitem2.md) an, das das Vorschaubild darstellt.

</dd> <dt>

*pWiaTransferCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Gibt einen Zeiger auf die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) der Anwendung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn eine Anwendung [**Download**](-wia-iwiatransfer-download.md) aufruft und wenn eine Anwendung die Funktion der WIA 2.0 Preview-Komponente `GetNewPreview` aufruft. **IWiaImageFilter::InitializeFilter** speichert die Verweise auf *pWiaItem2* und *pWiaTransferCallback,* um sie an diese Funktionen zu übergeben. Diese beiden Schnittstellenzeiger sollten als Membervariablen gespeichert werden, und [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sollte jeweils aufgerufen werden. Die Schnittstellenzeiger werden auch in der Implementierung des Filters von [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) und [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) während der Imageerfassung benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
