---
description: Die DoInitialize-Methode muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, um unmittelbar vor dem Aufruf der NPPs IRTCConnect-Methode einen Erfassungsfilter abzurufen.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: IMonitorDoInitialize-Methode (Netmon.h)
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
ms.openlocfilehash: 013a1604c1cbc709f35ac23378bab008d6c67f9053c171190b20669106303f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779180"
---
# <a name="imonitordoinitialize-method"></a>IMonitor::D oInitialize-Methode

Die **DoInitialize-Methode** muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, um unmittelbar vor dem Aufrufen der [IRTC::Verbinden-Methode](irtc-connect.md) des NPP einen Erfassungsfilter abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pUnkMonitorCtrl* \[ In\]
</dt> <dd>

Ein [IUnknown-Zeiger,](/windows/win32/api/unknwn/nn-unknwn-iunknown) der von MCSVC übergeben wird. Um eine unterstützte Monitorsteuerungsschnittstelle zu erhalten, muss der Monitor [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Zeiger aufrufen.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Handle für ein NPP-BLOB.

Bei der Ausgabe ein NPP-BLOB, das einen Erfassungsfilter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht NOERROR).

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Bei einem Fehler erstellt MCSVC den Monitor nicht und ruft [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nicht auf dem Schnittstellenzeiger auf.

## <a name="remarks"></a>Hinweise

McSVC ruft die **DoInitialize-Methode** auf, um alle erforderlichen Überwachungsinitialisierungen auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

