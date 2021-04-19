---
description: Der tatsächliche Anhaltevorgang wird durchgeführt, und es werden keine weiteren Aufrufe in das Modul zur Inhalts Entschlüsselung (CDM) durchgeführt.
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'IMF cdmsuspendnotify:: End-Methode'
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
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362414"
---
# <a name="imfcdmsuspendnotifyend-method"></a>IMF cdmsuspendnotify:: End-Methode

Der tatsächliche Anhaltevorgang wird durchgeführt, und es werden keine weiteren Aufrufe in das Modul zur Inhalts Entschlüsselung (CDM) durchgeführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF cdmsuspendnotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




