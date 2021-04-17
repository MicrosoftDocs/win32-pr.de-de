---
description: Ruft die Versionsnummer des Ereignis Systems ab.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2:: GetVersion-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483870"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2:: GetVersion-Methode

Ruft die Versionsnummer des Ereignis Systems ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnVersion* \[ vorgenommen\]
</dt> <dd>

Die Versionsnummer des Ereignis Systems.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




