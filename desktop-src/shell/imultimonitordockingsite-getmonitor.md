---
description: Ruft den aktuellen Standard Monitor ab.
title: 'Imultimonitordockingsite:: getmonitor-Methode'
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
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994943"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>Imultimonitordockingsite:: getmonitor-Methode

Ruft den aktuellen Standard Monitor ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*punksrc* \[ in\]
</dt> <dd>

Typ: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ein Zeiger auf das Objekt, das die [_ *idockingwindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert, für die der Monitor angefordert wird.

</dd> <dt>

*phmon* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **Hmonitor \** _

Wenn die Funktion zurückgegeben wird, enthält Sie einen Zeiger auf das Handle des Standard Monitors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |



 

 
