---
title: IWMDRMDevice2 getlicenerstate-Methode
description: Die getlicencstate-Methode ruft den Lizenzstatus ab.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Getlicencstate-Methode, Windows Media Device Manager
- Getlicencstate-Methode, Windows Media Device Manager, IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2-Schnittstelle Windows Media Device Manager, getlicenanstate-Methode
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
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355052"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2:: getlicenerstate-Methode

Die **getlicencstate** -Methode ruft den Lizenzstatus ab.

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

*pbstatus-erydata* \[ in\]
</dt> <dd>

Zeiger auf die abgefragten Daten des Lizenz Zustands.

</dd> <dt>

*cbstatuequerydata* \[ in\]
</dt> <dd>

Anzahl der abgefragten Daten.

</dd> <dt>

*pdwcategory* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Kategorie.

</dd> <dt>

*pkremainingcounts* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die verbleibenden Zähler.

</dd> <dt>

*pkremaininghours* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die verbleibenden Stunden.

</dd> <dt>

*pdwreserved* \[ vorgenommen\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode ist erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMDevice2-Schnittstelle**](iwmdrmdevice2.md)
</dt> </dl>

 

 





