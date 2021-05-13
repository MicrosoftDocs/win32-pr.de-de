---
description: Ändert, welcher Monitor für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet wird.
title: IMultiMonitorDockingSite::SetMonitor-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841941"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>IMultiMonitorDockingSite::SetMonitor-Methode

Ändert, welcher Monitor für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexSrc* \[ In\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ein Zeiger auf das -Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert, für die der Monitor geändert wird.

</dd> <dt>

*hMonNeu* \[ In\]
</dt> <dd>

Typ: **HMONITOR**

Ein Handle für den Monitor, der den vorhandenen Standardmonitor ersetzt.

</dd> <dt>

*phMonOld* \[ out\]
</dt> <dd>

Typ: **HMONITOR \***

Enthält nach der Rückgabe dieser Funktion einen Zeiger auf das Handle des vorherigen Standardmonitors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                   |



 

 
