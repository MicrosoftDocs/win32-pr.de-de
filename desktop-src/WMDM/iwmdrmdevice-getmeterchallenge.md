---
title: Methode ' iwmdrmdevice getmeterchallenge '
description: Die getmeterchallenge-Methode ruft die Messungs Herausforderung ab.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Getmeterchallenge-Methode, Windows Media Device Manager
- Getmeterchallenge-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getmeterchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364034"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>Iwmdrmdevice:: getmeterchallenge-Methode

Die **getmeterchallenge** -Methode ruft die Messungs Herausforderung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinmetercert* \[ in\]
</dt> <dd>

Das Messungs Zertifikat, das der Inhalts Besitzer zum Erfassen der zugeordneten Messungs Daten auf dem Gerät an den Host Computer sendet.

</dd> <dt>

*ppbmeterchallenge* \[ vorgenommen\]
</dt> <dd>

Ergebnis der abgerufenen Messungs Abfrage.

</dd> <dt>

*pcbmeterchallenge* \[ vorgenommen\]
</dt> <dd>

Die Größe der Messungs Herausforderung in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Messungs Daten werden im DRM-Datenspeicher auf dem Gerät für Inhalte mit aktivierter Messung gesammelt und gespeichert. Aktionen wie z. b. Play werden aufgezeichnet. Wenn diese Funktion aufgerufen wird, sammelt das Gerät die Messungs Daten im DRM-Datenspeicher in Form eines XML-Dokuments und sendet Sie an den Host Computer. Wenn zu viele Daten vorhanden sind, werden Sie in Phasen gesendet.

Wenn der Host Computer die Messungs Daten empfängt, sendet er die Daten über das Internet an die im Messungs Zertifikat angegebene URL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





