---
title: Iwmdrmlicenabacquisition-Methode (wmdrmsdk. h)
description: Die monitorlicensererwerbs-Methode initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Monitorlicenabacquisition-Methode Windows Media-Format
- Monitorlicenaberwerbs-Methode Windows Media-Format, iwmdrmlicenabsmanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, monitorliceneracquisition-Methode
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
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357305"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>Iwmdrmlicensmanagement:: monitorliceneracquisition-Methode

Die **monitorlicensererwerbs** -Methode initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.

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

*bstrinkid* \[ in\]
</dt> <dd>

Die Schlüssel-ID (Kid) der erworbenen Lizenz.

</dd> <dt>

*bstrauch Header* \[ in\]
</dt> <dd>

Inhalts Header, der im Aufrufen der [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode verwendet wurde.

</dd> <dt>

*bstractions* \[ in\]
</dt> <dd>

Zeichenfolge, die die im Aufrufen der **AcquireLicense** -Methode angeforderten Aktionen enthält.

</dd> <dt>

*ppunkcancelationcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert. Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





