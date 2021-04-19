---
title: Methode ' iwmdrmdevice ' getsecureclockchallenge
description: Die getsecureclockchallenge-Methode ruft das Challenge-Ergebnis der sicheren Uhr ab.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Getsecureclockchallenge-Methode, Windows Media Device Manager
- Getsecureclockchallenge-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsecureclockchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353790"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>Iwmdrmdevice:: getsecureclockchallenge-Methode

Die **getsecureclockchallenge** -Methode ruft das Challenge-Ergebnis der sicheren Uhr ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbchallenge* \[ vorgenommen\]
</dt> <dd>

Das Abfrageergebnis wurde abgerufen.

</dd> <dt>

*pcbchallenge* \[ vorgenommen\]
</dt> <dd>

Größe des Challenge-Ergebnisses in Bytes.

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

[**Getsecureclock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





