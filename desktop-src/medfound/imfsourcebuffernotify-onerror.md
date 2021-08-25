---
description: Wird verwendet, um anzugeben, dass beim Quellpuffer ein Fehler aufgetreten ist.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: DURCHSCHN. SourceBufferNotify::OnError-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 0602340011bae5af974a3441b42d62d392394b79854015acc68da0b1c2fcf538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957800"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>DURCHSCHN. SourceBufferNotify::OnError-Methode

Wird verwendet, um anzugeben, dass beim Quellpuffer ein Fehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hr* \[ In\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DURCHSCHN. SourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




