---
description: Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.
title: 'Imultimonitordockingsite:: setmonitor-Methode'
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
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995199"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>Imultimonitordockingsite:: setmonitor-Methode

Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.

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

*punksrc* \[ in\]
</dt> <dd>

Typ: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ein Zeiger auf das Objekt, das die [_ *idockingwindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert, für die der Monitor geändert wird.

</dd> <dt>

*hmonnew* \[ in\]
</dt> <dd>

Typ: **Hmonitor**

Ein Handle für den Monitor, der den vorhandenen Standard Monitor ersetzt.

</dd> <dt>

*phmonold* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **Hmonitor \** _

Diese Funktion gibt einen Zeiger auf das vorherige Standard Monitor Handle zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |



 

 
