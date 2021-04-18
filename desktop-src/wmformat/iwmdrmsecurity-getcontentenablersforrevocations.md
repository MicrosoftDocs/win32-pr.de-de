---
title: Iwmdrmsecurity getcontentenablersforrevocations-Methode (wmdrmsdk. h)
description: Die getcontentenablersforrevocations-Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Getcontentenablersforrevocations-Methode, Windows Media-Format
- Getcontentenablersforrevocations-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getcontentenablersforrevocations-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358376"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>Iwmdrmsecurity:: getcontentenablersforrevocations-Methode

Die **getcontentenablersforrevocations** -Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rgpbcerts* \[ in\]
</dt> <dd>

Ein Array von Zertifikaten, für die Inhalts Enabler abgerufen werden sollen. Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden.

</dd> <dt>

*rgpdwcertsizes* \[ in\]
</dt> <dd>

Ein Array, das die Größe der Zertifikate im *rgpbcerts* -Array enthält. Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden.

</dd> <dt>

*rgpguidcerts* \[ in\]
</dt> <dd>

Ein Array, das die Typen der Zertifikate im *rgpbcerts* -Array enthält. Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden. Verwenden Sie für jedes Element des Arrays einen der folgenden Werte.



| GUID-Konstante                 | BESCHREIBUNG                                                    |
|-------------------------------|----------------------------------------------------------------|
| WMDRM- \_ revocationtype- \_ App    | Gibt ein Anwendungs Zertifikat an.                          |
| WMDRM- \_ revocationtype- \_ Gerät | Gibt ein Gerätezertifikat an.                                |
| WMDRM \_ revocationtype \_ Cardea | Gibt ein Windows Media DRM für Netzwerkgeräte Zertifikat an. |



 

</dd> <dt>

*ccerts* \[ in\]
</dt> <dd>

Anzahl von Zertifikaten, für die Inhalts Enabler abgerufen werden sollen. Dies ist die Anzahl der Elemente im *rgpbcerts* -Array, des *rgpdwcertsizes* -Arrays und des *rgpguidcerts* -Arrays.

</dd> <dt>

*hresulthint* \[ in\]
</dt> <dd>

Rückgabewert, der von dem Vorgang empfangen wurde, der aufgrund eines gesperrten Zertifikats nicht erfolgreich war. Wenn Sie nicht als Antwort auf einen fehlgeschlagenen Methodenaufruf aufrufen, legen Sie auf \_ OK fest.

</dd> <dt>

*prgcontentenablers* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die Adressen der neu erstellten **IMF contentenabler** -Schnittstellen empfängt. Legen Sie diese Einstellung auf **null** fest, um die Anzahl der Inhalts-Enabler im *pccontentenablers* -Parameter zu erhalten.

</dd> <dt>

*pccontentenablers* \[ in, out\]
</dt> <dd>

Anzahl der Elemente im *prgcontentenablers* -Array. Wenn *prgcontentenablers* den Wert **null** hat, wird dieser Wert auf die Anzahl der benötigten Inhalts-Enabler bei der Ausgabe festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die **imfcontentenabler** -Schnittstelle zum Erneuern von widerrufenen Komponenten verwenden, müssen Sie den Prozess für den Benutzer verdeutlichen. Diese Erläuterung muss vorgenommen werden, da der Aktualisierungsprozess Informationen vom Client Computer an eine Microsoft-Website sendet.

Wenn Sie **imfcontentenabler:: automaticenable** aufgerufen haben, wird der Standardbrowser von Content Wegbereiter mit der Adresse des Aktualisierungs Diensts auf der Microsoft-Website gestartet. Ein eindeutiger Bezeichner, der die widerrufene Komponente identifiziert, wird an den Aktualisierungs Dienst gesendet. Der Dienst leitet dann den Browser an eine Webseite weiter, von der aus der Benutzer die neue Version der gesperrten Komponente herunterladen und installieren kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Automatisierte Sperrung und Erneuerung von Komponenten**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





