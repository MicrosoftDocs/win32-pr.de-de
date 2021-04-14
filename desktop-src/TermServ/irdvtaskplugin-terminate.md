---
title: Undvtaskplugin-Beendigungs Methode
description: Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Beendigungs Methode Remotedesktopdienste
- Methode Remotedesktopdienste beenden, Schnittstelle "iridvtaskplugin"
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Methode beenden
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392019"
---
# <a name="irdvtaskpluginterminate-method"></a>Undvtaskplugin:: End-Methode

Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Personalabteilung* \[ in\]
</dt> <dd>

Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist. Wenn das Herunterfahren normal ist, enthält dies **S \_ OK**. Andernfalls enthält Sie einen **HRESULT** -Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Undvtaskplugin"**](irdvtaskplugin.md)
</dt> </dl>

 

 





