---
title: Iwmdrmdevice getdevicecertificate-Methode
description: Die getdevicecertificate-Methode ruft das Gerätezertifikat ab.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Getdevicecertificate-Methode, Windows Media Device Manager
- Getdevicecertificate-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getdevicecertificate-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357311"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a>Iwmdrmdevice:: getdevicecertificate-Methode

Die **getdevicecertificate** -Methode ruft das Gerätezertifikat ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstraudevcert* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der das abgerufene Gerätezertifikat enthält.

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

 

 





