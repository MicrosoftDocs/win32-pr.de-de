---
title: IWMDRMDevice GetSyncList-Methode
description: Die GetSyncList-Methode ruft die Lizenzsynchronisierungsliste auf dem Gerät ab. Mit der Lizenzsynchronisierung kann der Hostcomputer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- GetSyncList-Methode windows Media Geräte-Manager
- GetSyncList-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , GetSyncList method
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6424daa720f9987228175a7698a29f7056e5d4b4d174d1d635bbcd1ed7f8382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619580"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>IWMDRMDevice::GetSyncList-Methode

Die **GetSyncList-Methode** ruft die Lizenzsynchronisierungsliste auf dem Gerät ab. Mit der Lizenzsynchronisierung kann der Hostcomputer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cMinCountThreshold* \[ In\]
</dt> <dd>

Mindestanzahlschwellenwert.

</dd> <dt>

*cMinHoursThreshold* \[ In\]
</dt> <dd>

Mindestschwellenwert für Stunden.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Die Liste der abgerufenen Lizenzsynchronisierungen.

</dd> <dt>

*listenSyncList* \[ out\]
</dt> <dd>

Größe der Lizenzsynchronisierungsliste in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





