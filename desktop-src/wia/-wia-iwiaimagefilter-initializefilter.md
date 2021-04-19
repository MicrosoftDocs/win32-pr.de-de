---
description: Initialisiert den Filter. Wird von der Windows-Abbild Beschaffung (WIA) 2,0 vor jedem Herunterladen des Images aufgerufen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Iwiaimagefilter:: initializefilter-Methode (WIA. h)'
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
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359059"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Iwiaimagefilter:: initializefilter-Methode

Initialisiert den Filter. Wird von der Windows-Abbild Beschaffung (WIA) 2,0 vor jedem Herunterladen des Images aufgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWiaItem2* \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Gibt einen Zeiger auf das [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Element an, das das Vorschaubild darstellt.

</dd> <dt>

*pwiatransfercallback* \[ in\]
</dt> <dd>

Typ: **[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _

Gibt einen Zeiger auf die [_ *iwiatransfercallback* *](-wia-iwiatransfercallback.md) -Schnittstelle der Anwendung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn eine Anwendung den [**Download**](-wia-iwiatransfer-download.md) aufruft und eine Anwendung die Funktion der WIA 2,0-Vorschau Komponente aufruft `GetNewPreview` . **Iwiaimagefilter:: initializefilter** speichert die Verweise auf *pWiaItem2* und *pwiatransfercallback* , um diese Funktionen zu übergeben. Diese beiden Schnittstellen Zeiger sollten als Element Variablen gespeichert werden, und [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sollte für jede aufgerufen werden. Die Schnittstellen Zeiger werden auch in der Implementierung von " [**transfercallback**](-wia-iwiatransfercallback-transfercallback.md) " und " [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) " des Filters während der Abbild Erfassung benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
