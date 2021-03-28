---
description: Überprüft, ob der Monitor aktiv und verfügbar ist.
title: 'Imultimonitordockingsite:: RequestMonitor-Methode'
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
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960945"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>Imultimonitordockingsite:: RequestMonitor-Methode

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

*punksrc* \[ in\]
</dt> <dd>

Typ: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ein Zeiger auf das Objekt, das die [_ *idockingwindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert.

</dd> <dt>

*phmon* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **Hmonitor \** _

Ein Zeiger auf das Handle des Standard Monitors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |



 

 
