---
description: Überprüft, ob der Monitor aktiv und verfügbar ist.
title: IMultiMonitorDockingSite::RequestMonitor-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 9e5eeb2b99455d81bae36f1c5f26ed38126122bb58a5b8964a47cfb205f71ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942900"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>IMultiMonitorDockingSite::RequestMonitor-Methode

Überprüft, ob der Monitor aktiv und verfügbar ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexSrc* \[ In\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ein Zeiger auf das -Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert.

</dd> <dt>

*phMon* \[ In\]
</dt> <dd>

Typ: **HMONITOR \***

Ein Zeiger auf das Handle des Standardmonitors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |



 

 
