---
description: Legt einen neuen Anwendungs Rückruf für den Bild Verarbeitungs Filter fest, der für Weiterleitungs Aufrufe verwendet werden soll.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Iwiaimagefilter:: setnewcallback-Methode (WIA. h)'
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
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752832"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>Iwiaimagefilter:: setnewcallback-Methode

Legt einen neuen Anwendungs Rückruf für den Bild Verarbeitungs Filter fest, der für Weiterleitungs Aufrufe verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwiatransfercallback* \[ in\]
</dt> <dd>

Typ: **[ **iwiatransfercallback**](-wia-iwiatransfercallback.md)**

Gibt einen Zeiger auf die [**iwiatransfercallback**](-wia-iwiatransfercallback.md) -Schnittstelle der Anwendung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nennen Sie diese Methode nicht direkt aus der Anwendung.

Der Bild Verarbeitungs Filter ist erforderlich, um die zuvor gespeicherte Anwendungs Rückruf Schnittstelle vor dem Festlegen des neuen Rückrufs freizugeben.

Wenn *pwiatransfercallback* **null** ist, sollte der Bild Verarbeitungs Filter einfach den alten Anwendungs Rückruf freigeben und S OK zurückgeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




