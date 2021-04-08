---
title: IWMPEvents4 syncschätzationcomplete-Methode
description: Das syncschätzationcomplete-Ereignis tritt auf, wenn eine von IWMPSyncDevice3 estimatesyncsize initiierte Größen Schätzung beendet ist.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Syncschätzationcomplete-Methode, Windows-Media Player
- Syncschätzationcomplete-Methode, Windows Media Player, IWMPEvents4-Schnittstelle
- IWMPEvents4 Interface, Windows Media Player, syncschätzationcomplete-Methode
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723384"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4:: syncschätzationcomplete-Methode

Das **syncschätzationcomplete** -Ereignis tritt auf, wenn eine von [**IWMPSyncDevice3:: estimatesyncsize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)initiierte Größen Schätzung beendet ist.

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

*pdevice* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**iwmpsyncdevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) -Schnittstelle, die das Gerät darstellt, für das die Größen Schätzung initiiert wurde.

</dd> <dt>

*hrresult* \[ in\]
</dt> <dd>

Ein-Wert, der den Erfolg oder Misserfolg der Schätzung angibt.



| Wert                                                                                                                                       | Bedeutung                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>          | Die Schätzung war erfolgreich.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ Abbrechen**</dt> </dl> | Die Schätzung wurde abgebrochen.<br/> |



 

</dd> <dt>

*lestimatedusedspace* \[ in\]
</dt> <dd>

Der geschätzte Speicherplatz (in Bytes), der auf dem Gerät verwendet wird.

</dd> <dt>

*lestimatedsize* \[ in\]
</dt> <dd>

Die geschätzte Größe der zu synchronisierenden Daten (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPEvents4-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3:: estimatesyncsize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





