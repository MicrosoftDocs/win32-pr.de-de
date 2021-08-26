---
description: Der tatsächliche Suspend wird in Arbeit kommen, und es werden keine aufruften mehr an das Content Decryption Module (CDM) vorgenommen.
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: DURCHSCHN.CdmSuspendNotify::End-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9ad64b4b02c6accae3749478e09dee6078050bf22c0b1e5d13e4d1ea37f1635c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957910"
---
# <a name="imfcdmsuspendnotifyend-method"></a>DURCHSCHN.CdmSuspendNotify::End-Methode

Der tatsächliche Suspend wird in Arbeit kommen, und es werden keine aufruften mehr an das Content Decryption Module (CDM) vorgenommen.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BESCHRIFTUNGCdmSuspendNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




