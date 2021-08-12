---
title: IWMPEvents4 SyncEstimationComplete-Methode
description: Das SyncEstimationComplete-Ereignis tritt auf, wenn eine Größenschätzung, die zuvor von IWMPSyncDevice3 estimateSyncSize initiiert wurde, abgeschlossen ist.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- SyncEstimationComplete-Methode Windows Media Player
- SyncEstimationComplete-Methode Windows Media Player , IWMPEvents4-Schnittstelle
- IWMPEvents4-Schnittstelle Windows Media Player , SyncEstimationComplete-Methode
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3f444cdc66874c907bb4c6412fa10384fde67145563d79153c28cb675c6fc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575605"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4::SyncEstimationComplete-Methode

Das **SyncEstimationComplete-Ereignis** tritt auf, wenn eine Größenschätzung, die zuvor von [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)initiiert wurde, abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Zeiger auf die [**IWMPSyncDevice-Schnittstelle,**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) die das Gerät darstellt, für das die Größenschätzung initiiert wurde.

</dd> <dt>

*hrResult* \[ In\]
</dt> <dd>

Ein -Wert, der den Erfolg oder Fehler der Schätzung angibt.



| Wert                                                                                                                                       | Bedeutung                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>          | Die Schätzung war erfolgreich.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ ABORT**</dt> </dl> | Die Schätzung wurde abgebrochen.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ In\]
</dt> <dd>

Der geschätzte Speicherplatz (in Bytes), der auf dem Gerät verwendet wird.

</dd> <dt>

*lEstimatedSize* \[ In\]
</dt> <dd>

Die geschätzte Größe (in Bytes) der zu synchronisierenden Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPEvents4-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





