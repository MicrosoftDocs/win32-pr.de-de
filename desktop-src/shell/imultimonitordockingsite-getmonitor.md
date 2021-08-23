---
description: Ruft den aktuellen Standardmonitor ab.
title: IMultiMonitorDockingSite::GetMonitor-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 63609dc545e8f69ae2023e6659158297a65fdb7b549071126702b163c04555f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661890"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>IMultiMonitorDockingSite::GetMonitor-Methode

Ruft den aktuellen Standardmonitor ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexSrc* \[ In\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ein Zeiger auf das -Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert, für die der Monitor angefordert wird.

</dd> <dt>

*phMon* \[ out\]
</dt> <dd>

Typ: **HMONITOR \***

Enthält nach der Rückgabe der Funktion einen Zeiger auf das Handle des Standardmonitors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |



 

 
