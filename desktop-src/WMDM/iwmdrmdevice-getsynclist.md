---
title: Methode "iwmdrmdevice getsynclist"
description: Die getsynclist-Methode ruft die Lizenz Synchronisierungs Liste auf dem Gerät ab. Mit der Lizenz Synchronisierung kann der Host Computer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Getsynclist-Methode, Windows Media Device Manager
- Getsynclist-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsynclist-Methode
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
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356446"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>Iwmdrmdevice:: getsynclist-Methode

Die **getsynclist** -Methode ruft die Lizenz Synchronisierungs Liste auf dem Gerät ab. Mit der Lizenz Synchronisierung kann der Host Computer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.

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

*cminzählthreshold* \[ in\]
</dt> <dd>

Schwellenwert für minimale Anzahl.

</dd> <dt>

*cminhoursthreshold* \[ in\]
</dt> <dd>

Schwellenwert für minimale Stunden.

</dd> <dt>

*ppbsynclist* \[ vorgenommen\]
</dt> <dd>

Abgerufene Lizenz Synchronisierungs Liste.

</dd> <dt>

*pcbsynclist* \[ vorgenommen\]
</dt> <dd>

Größe der Lizenz Synchronisierungs Liste in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





