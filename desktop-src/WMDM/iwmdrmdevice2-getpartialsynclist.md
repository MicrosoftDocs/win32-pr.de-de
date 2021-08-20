---
title: IWMDRMDevice2 GetPartialSyncList-Methode
description: Die GetPartialSyncList-Methode ruft eine Teilsynchronisierungsliste ab.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- GetPartialSyncList-Methode windows Media Geräte-Manager
- GetPartialSyncList-Methode windows Media Geräte-Manager , IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2-Schnittstelle windows Media Geräte-Manager , GetPartialSyncList-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0bcff91d41ce77003219336431433ee511ff144dfcb8be7880526994689a929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055658"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2::GetPartialSyncList-Methode

Die **GetPartialSyncList-Methode** ruft eine Teilsynchronisierungsliste ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
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

*dwStartingIndex* \[ In\]
</dt> <dd>

Startposition für die Indizierung.

</dd> <dt>

*cItems* \[ In\]
</dt> <dd>

Anzahl der zu indizierten Elemente.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Die Liste der abgerufenen Lizenzsynchronisierungen.

</dd> <dt>

*listenSyncList* \[ out\]
</dt> <dd>

Größe der Lizenzsynchronisierungsliste in Bytes.

</dd> <dt>

*pdwNextStartingIndex* \[ out\]
</dt> <dd>

Nächste Startposition für die Indizierung.

</dd> <dt>

*pcItemsProcessed* \[ out\]
</dt> <dd>

Anzahl der elemente, die verarbeitet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Alle Schnittstellenmethoden in Windows Media Geräte-Manager können eine der folgenden Klassen von Fehlercodes zurückgeben:

-   COM-Standardfehlercodes
-   Windows in HRESULT-Werte konvertierte Fehlercodes
-   Windows Media Geräte-Manager-Fehlercodes

Eine umfassende Liste möglicher Fehlercodes finden Sie unter [Fehlercodes](error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**IWMDRMDevice2-Schnittstelle**](iwmdrmdevice2.md)
</dt> </dl>

 

 





