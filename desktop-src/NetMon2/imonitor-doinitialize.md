---
description: Die doinitialize-Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um unmittelbar vor dem Aufrufen der NPPs-Methode "untcconnect" einen Erfassungs Filter zu erhalten.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Imonitordoinitialize-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525115"
---
# <a name="imonitordoinitialize-method"></a>Imonitor::D oinitialize-Methode

Die **doinitialize** -Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um einen Erfassungs Filter direkt vor dem Aufrufen der " [untc:: Connect](irtc-connect.md) "-Methode von NPP abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*punkmonitorctrl* \[ in\]
</dt> <dd>

Ein [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger, der von mcsvc übermittelt wurde. Um eine unterstützte Monitor Steuerungs Schnittstelle zu erhalten, muss der Monitor [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Zeiger abrufen.

</dd> <dt>

*hnppblob* \[ in, out\]
</dt> <dd>

Bei Eingabe ein Handle für ein NPP-BLOB.

Bei der Ausgabe ein NPP-BLOB, das einen Erfassungs Filter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Bei einem Fehler erstellt der mcsvc den Monitor nicht, oder der Befehl [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) wird nicht auf dem Schnittstellen Zeiger aufgerufen.

## <a name="remarks"></a>Bemerkungen

Die mcsvc Ruft die **doinitialize** -Methode auf, um die erforderliche Monitor Initialisierung auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

