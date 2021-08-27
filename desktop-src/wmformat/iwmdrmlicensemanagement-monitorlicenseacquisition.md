---
title: IWMDRMLicenseManagement MonitorLicenseAcquisition-Methode (Wmdrmsdk.h)
description: Die MonitorLicenseAcquisition-Methode initiiert die Überwachung für einen Lizenzerwerbsprozess.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- MonitorLicenseAcquisition-Methode windows Media Format
- MonitorLicenseAcquisition-Methode windows Media Format , IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , MonitorLicenseAcquisition-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027578"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>IWMDRMLicenseManagement::MonitorLicenseAcquisition-Methode

Die **MonitorLicenseAcquisition-Methode** initiiert die Überwachung für einen Lizenzerwerbsprozess.

## <a name="syntax"></a>Syntax


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Schlüssel-ID (KEY ID, KID) der erworbenen Lizenz.

</dd> <dt>

*bstrHeader* \[ In\]
</dt> <dd>

Inhaltsheader, der beim Aufruf der [**AcquireLicense-Methode**](iwmdrmlicensemanagement-acquirelicense.md) verwendet wurde.

</dd> <dt>

*bstrActions* \[ In\]
</dt> <dd>

Zeichenfolge, die die aktionen enthält, die im Aufruf der **AcquireLicense-Methode** angefordert werden.

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Zeiger, der einen Zeiger auf die **IUnknown-Schnittstelle** eines Objekts empfängt, das diesen asynchronen Aufruf identifiziert. Dieser Schnittstellenzeiger kann verwendet werden, um den asynchronen Aufruf abzubrechen, indem die [**IWMDRMEventGenerator::CancelAsyncOperation-Methode**](iwmdrmeventgenerator-cancelasyncoperation.md) aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





