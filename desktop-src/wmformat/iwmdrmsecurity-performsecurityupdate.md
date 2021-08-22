---
title: IWMDRMSecurity PerformSecurityUpdate-Methode (Wmdrmsdk.h)
description: Die PerformSecurityUpdate-Methode initiiert ein Sicherheitsupdate für das DRM-Subsystem auf dem lokalen Computer.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- PerformSecurityUpdate-Methode windows Media Format
- PerformSecurityUpdate-Methode windows Media Format , IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity-Schnittstelle windows Media Format , PerformSecurityUpdate-Methode
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
ms.openlocfilehash: 8521497c1e2bca1bb2ae11349a4829c22c8b092a4cd0034008b314a7b69adb6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707900"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity::P erformSecurityUpdate-Methode

Die **PerformSecurityUpdate-Methode** initiiert ein Sicherheitsupdate für das DRM-Subsystem auf dem lokalen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Die Updateoption wird als eines der folgenden Flags ausgedrückt.



| Flag                                          | Beschreibung                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| WMDRM \_ SECURITY \_ PERFORM \_ INDIV               | Bewirkt, dass die DRM-Komponente nur individualisiert wird, wenn die Version des Clients veraltet ist. |
| WMDRM \_ SECURITY \_ PERFORM \_ REVOCATION \_ REFRESH | Bewirkt, dass die Sperrlisten auf dem Clientcomputer aktualisiert werden.                               |
| WMDRM \_ SECURITY \_ PERFORM \_ FORCE \_ INDIV        | Bewirkt, dass die DRM-Komponente individualisiert wird, auch wenn die Version des Clients auf dem neuesten Stand ist.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf ein Objekt empfängt, das zum Abbrechen dieses Vorgangs verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Sie gibt sofort nach dem Aufruf zurück und generiert dann Ereignisse, die vom im *dwFlags-Parameter* festgelegten Flag abhängen.

Für die Individualisierung (Flag auf WMDRM \_ SECURITY \_ PERFORM \_ INDIV oder WMDRM \_ SECURITY PERFORM FORCE \_ \_ \_ INDIV festgelegt) wird eine Reihe von **MEWMDRMIndividualizationProgress-Ereignissen** generiert, gefolgt von einem **MEWMDRMIndividualizationCompleted-Ereignis,** wenn die Verarbeitung abgeschlossen ist. Der Wert jedes **MEWMDRMIndividualizationProgress-Ereignisses,** das durch Aufrufen von **"POINTERMediaEvent::GetValue"** abgerufen wird, ist ein **IUnknown-Zeiger.** Sie können die **QueryInterface-Methode** der abgerufenen **IUnknown-Schnittstelle** aufrufen, um eine Instanz der [**IWMDRMIndividualizationStatus-Schnittstelle**](iwmdrmindividualizationstatus.md) abzurufen.

Zum Aktualisieren der Sperrlisten (Flag auf WMDRM SECURITY PERFORM REVOCATION REFRESH festgelegt) wird nach Abschluss der \_ Verarbeitung ein \_ \_ \_ **MEWMDRMREvocationDownloadCompleted-Ereignis** generiert.

> [!Note]  
> Wenn **PerformSecurityUpdate** die Individualisierung abschließt, sind die einzigen vorhandenen Objekte, die den neuen individualisierten Zustand widerspiegeln, diejenigen, die von **IWMDRMSecurity** erben. Alle anderen vorhandenen Objekte werden nicht aktualisiert. Sie müssen alle anderen Objekte freigeben und neu erstellen, damit sie den neuen individualisierten Zustand widerspiegeln.

 

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation Ereignismodells.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Automatisierte Komponentensperrung und -verlängerung**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Beispiel für die DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**Durchführen der DRM-Individualisierung**](performing-drm-individualization.md)
</dt> </dl>

 

 





