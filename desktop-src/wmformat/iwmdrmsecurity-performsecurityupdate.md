---
title: Iwmdrmsecurity performsecurityupdate-Methode (wmdrmsdk. h)
description: Die performsecurityupdate-Methode initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem lokalen Computer.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Performsecurityupdate-Methode Windows Media-Format
- Performsecurityupdate-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, performsecurityupdate-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364603"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>Iwmdrmsecurity::P erformsecurityupdate-Methode

Die **performsecurityupdate** -Methode initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem lokalen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Die Update Option wurde als eines der folgenden Flags ausgedrückt.



| Flag                                          | Beschreibung                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| WMDRM- \_ Sicherheit \_ Durchführen von \_ indiv               | Bewirkt, dass die DRM-Komponente nur dann individualisiert wird, wenn die Version des Clients veraltet ist. |
| WMDRM- \_ Sicherheit \_ Durchführen der Sperr \_ \_ Aktualisierung | Bewirkt, dass die Sperr Listen auf dem Client Computer aktualisiert werden.                               |
| WMDRM- \_ Sicherheit \_ Durchführen von Force- \_ \_ indiv        | Bewirkt, dass die DRM-Komponente individuell ist, auch wenn die Version des Clients auf dem neuesten Stand ist.  |



 

</dd> <dt>

*ppunkcancelationcookie* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf ein Objekt empfängt, das verwendet werden kann, um diesen Vorgang abzubrechen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird asynchron ausgeführt. Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann Ereignisse, abhängig von dem im *dwFlags* -Parameter festgelegten Flag.

Für die individuelle Authentifizierung (Flag ist auf WMDRM- \_ Sicherheit \_ Durchführen von \_ indiv oder WMDRM \_ Security do \_ \_ Force \_ indiv festgelegt) wird eine Reihe von **mewmdrmindividualizationprogress** -Ereignissen generiert, gefolgt von einem **mewmdrmindividualizationcomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist. Der Wert jedes **mewmdrmindividualizationprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger. Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle aufzurufen, um eine Instanz der [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstelle zu erhalten.

Zum Aktualisieren der Sperr Listen (Flag ist auf WMDRM- \_ Sicherheit durchführen der Sperr Aktualisierung festgelegt \_ \_ \_ ) wird ein **mewmdrmrevocationdownloadcomplete** -Ereignis generiert, wenn die Verarbeitung abgeschlossen ist.

> [!Note]  
> Wenn **performsecurityupdate** die Individualisierung abschließt, sind die einzigen Objekte, die den neuen, individualisierten Zustand widerspiegeln, diejenigen, die von **iwmdrmsecurity** erben. Alle anderen vorhandenen Objekte werden nicht aktualisiert. Sie müssen alle anderen Objekte freigeben und neu erstellen, damit Sie den neuen, individualisierten Zustand widerspiegeln.

 

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Automatisierte Sperrung und Erneuerung von Komponenten**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Beispiel für DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**Durchführen der DRM-Individualisierung**](performing-drm-individualization.md)
</dt> </dl>

 

 





