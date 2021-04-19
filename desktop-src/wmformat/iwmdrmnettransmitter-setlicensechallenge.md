---
title: Iwmdrmnettransmitter setlicensechallenge-Methode (wmdrmsdk. h)
description: Die setlicensechallenge-Methode verarbeitet eine Lizenz Herausforderung, die von einem Windows Media DRM für den Empfänger von Netzwerkgeräten gesendet wird.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Setlicensechallenge-Methode, Windows Media-Format
- Setlicensechallenge-Methode Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, setlicensechallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367582"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Iwmdrmnettransmitter:: setlicensechallenge-Methode

Die **setlicensechallenge** -Methode verarbeitet eine Lizenz Herausforderung, die von einem Windows Media DRM für den Empfänger von Netzwerkgeräten gesendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pblicenabchallenge* \[ in\]
</dt> <dd>

Zeiger auf die Lizenz Aufforderungs Daten, die von einem Empfänger gesendet wurden.

</dd> <dt>

*cblicenanchallenge* \[ in\]
</dt> <dd>

Die Größe der Lizenz Herausforderung in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode erfolgreich ausgeführt wird, werden bei nachfolgenden Aufrufen der anderen Methoden von **iwmdrmnettransmitter** die Informationen in der verarbeiteten Abfrage verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnettransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





