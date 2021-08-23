---
description: Legt einen neuen Anwendungsrückruf für den Bildverarbeitungsfilter fest, der zum Weiterleiten von Aufrufen verwendet werden soll.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: IWiaImageFilter::SetNewCallback-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450490"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>IWiaImageFilter::SetNewCallback-Methode

Legt einen neuen Anwendungsrückruf für den Bildverarbeitungsfilter fest, der zum Weiterleiten von Aufrufen verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWiaTransferCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Gibt einen Zeiger auf die [**IWiaTransferCallback-Schnittstelle der Anwendung**](-wia-iwiatransfercallback.md) an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht direkt aus Ihrer Anwendung auf.

Der Bildverarbeitungsfilter ist erforderlich, um die zuvor gespeicherte Anwendungsrückrufschnittstelle vor dem Festlegen des neuen Rückrufs frei zu geben.

Wenn *pWiaTransferCallback* **NULL ist,** sollte der Bildverarbeitungsfilter einfach den alten Anwendungsrückruf veröffentlichen und S \_ OK zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




