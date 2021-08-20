---
title: IRDVTaskPlugin Terminate-Methode
description: Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Terminate-Methode Remotedesktopdienste
- Terminate-Methode Remotedesktopdienste , IRDVTaskPlugin-Schnittstelle
- IRDVTaskPlugin-Schnittstelle Remotedesktopdienste , Terminate-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ccfcb1a59f0db6d29881d139d16bd08308a40df2c1233beab66b0b4814caa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129267"
---
# <a name="irdvtaskpluginterminate-method"></a>IRDVTaskPlugin::Terminate-Methode

Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hr* \[ In\]
</dt> <dd>

Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist. Wenn das Herunterfahren normal ist, enthält **dies S \_ OK**. Andernfalls enthält  sie einen HRESULT-Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





