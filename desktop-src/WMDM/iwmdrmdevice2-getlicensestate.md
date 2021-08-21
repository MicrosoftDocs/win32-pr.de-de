---
title: IWMDRMDevice2 GetLicenseState-Methode
description: Die GetLicenseState-Methode ruft den Lizenzzustand ab.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- GetLicenseState-Methode windows Media Geräte-Manager
- GetLicenseState-Methode windows Media Geräte-Manager , IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2-Schnittstelle windows Media Geräte-Manager , GetLicenseState-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e068d537f460053800b0d52d667ba39b0577d717b08f83794a73b2bf8c854aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055698"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2::GetLicenseState-Methode

Die **GetLicenseState-Methode** ruft den Lizenzzustand ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbStateQueryData* \[ In\]
</dt> <dd>

Zeiger auf die abgefragten Daten des Lizenzstatus.

</dd> <dt>

*cbStateQueryData* \[ In\]
</dt> <dd>

Anzahl der abgefragten Daten.

</dd> <dt>

*pdwCategory* \[ out\]
</dt> <dd>

Zeiger auf die Kategorie.

</dd> <dt>

*pcRemainingCounts* \[ out\]
</dt> <dd>

Zeiger auf die verbleibenden Anzahlen.

</dd> <dt>

*pcRemainingHours* \[ out\]
</dt> <dd>

Zeiger auf die verbleibenden Stunden.

</dd> <dt>

*pdwReserved* \[ out\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode ist erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMDevice2-Schnittstelle**](iwmdrmdevice2.md)
</dt> </dl>

 

 





