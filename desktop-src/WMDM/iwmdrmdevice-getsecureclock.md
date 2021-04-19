---
title: "' Iwmdrmdevice ' getsecureclock-Methode"
description: Die getsecureclock-Methode ruft die sichere Uhr ab. Daher können zeitbasierte Lizenzen erzwungen werden.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Getsecureclock-Methode, Windows Media Device Manager
- Getsecureclock-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsecureclock-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367420"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>Iwmdrmdevice:: getsecureclock-Methode

Die **getsecureclock** -Methode ruft die sichere Uhr ab. Daher können zeitbasierte Lizenzen erzwungen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbsecureclock* \[ vorgenommen\]
</dt> <dd>

Die sichere Uhr wurde abgerufen.

</dd> <dt>

*pcbsecureclock* \[ vorgenommen\]
</dt> <dd>

Größe der sicheren Uhr (in Bytes).

</dd> <dt>

*pdwflags* \[ vorgenommen\]
</dt> <dd>

Gerätestatusflags. Bei diesem Wert muss es sich um eines der folgenden Flags handeln.



| Flag                     | Beschreibung                            |
|--------------------------|----------------------------------------|
| WMDRM- \_ Gerät \_ iswmdrm   | Das Gerät unterstützt Windows Media DRM. |
| WMDRM- \_ Geräte- \_ needclock | Das Gerät benötigt die Uhr.                |
| WMDRM- \_ Gerät gesperrt \_   | Das Gerät wurde widerrufen.           |



 

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

[**Getsecureclockchallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> <dt>

[**Setsecureclockresponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





