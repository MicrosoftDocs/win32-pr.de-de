---
title: IWMDRMLicenseManagement AcquireLicense-Methode (Wmdrmsdk.h)
description: Die AcquireLicense-Methode erhält asynchron eine Lizenz von einer angegebenen URL.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- 'AcquireLicense-Methode : Windows Media Format'
- AcquireLicense-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , AcquireLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad8251650c8a7e16c6eb2fc957df5e70459239c0cd6cf1184b5209ae51b6aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701126"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>IWMDRMLicenseManagement::AcquireLicense-Methode

Die **AcquireLicense-Methode** erhält asynchron eine Lizenz von einer angegebenen URL.

## <a name="syntax"></a>Syntax


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrURL* \[ In\]
</dt> <dd>

URL des Lizenzservers, von dem die Lizenz erworben werden soll. Übergeben **Sie NULL,** damit die Methode die URL aus dem Inhaltsheader analysiert.

</dd> <dt>

*bstrHeaderData* \[ In\]
</dt> <dd>

Inhaltsheader, der an den Lizenzserver übergeben werden soll. Wenn *bstrURL* NULL **ist,** analysiert die Methode die URL aus diesem Header. Wenn *dwFlags* auf WMDRM ACQUIRE LICENSE LEGACY NONSILENT festgelegt ist, legen Sie diesen Wert auf die Schlüssel-ID statt auf den \_ \_ gesamten \_ \_ Inhaltsheader fest.

</dd> <dt>

*bstrActions* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die 0 (null) oder mehr Aktionen enthält, für die die Berechtigung in der Lizenz anfordern werden soll. Die Zeichenfolge muss wie folgt formatiert sein:

-   Jede Aktion muss innerhalb eines ACTION-Elements definiert werden. Die Daten des Elements sind die Aktionszeichenfolge.
-   Alle ACTION-Elemente müssen in einem ACTIONLIST-Element enthalten sein.

    Die Zeichenfolge zum Anfordern einer Lizenz für die Wiedergabe von Inhalten ist beispielsweise wie die folgende formatiert:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags für Lizenzerwerbsoption. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| Konstante                                   | Beschreibung                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ ACQUIRE \_ LICENSE \_ SILENT            | Die Lizenz wird ohne Bestätigung durch die Clientanwendung direkt über das Internet ausgestellt.              |
| WMDRM \_ ACQUIRE \_ LICENSE \_ NONSILENT         | Das DRM-Subsystem erstellt eine Lizenzanforderung, die asynchron für die Veröffentlichung auf dem Lizenzserver zurückgegeben wird. |
| WMDRM \_ ACQUIRE \_ LICENSE \_ LEGACY \_ NONSILENT | Identisch mit WMDRM \_ ACQUIRE \_ LICENSE NONSILENT, mit der Ausnahme, dass eine DRM-Lizenzausforderung der Version \_ 1 erstellt wird.           |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Zeiger, der einen Zeiger auf die **IUnknown-Schnittstelle** eines Objekts empfängt, das diesen asynchronen Aufruf identifiziert. Dieser Schnittstellenzeiger kann verwendet werden, um den asynchronen Aufruf abzubricht, indem die [**IWMDRMEventGenerator::CancelAsyncOperation-Methode aufgerufen**](iwmdrmeventgenerator-cancelasyncoperation.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Er wird unmittelbar nach dem Aufgerufenen zurückgegeben und generiert dann ein **MEWMDRMLicenseAcquisitionCompleted-Ereignis,** wenn die Verarbeitung abgeschlossen ist. Bei Nicht-automatischen Lizenzerwerbsvorgängen ist der Wert des Ereignisses, das durch Aufrufen **vonGEFmediaEvent::GetValue** ermittelt wird, ein **IUnknown-Zeiger.** Sie können die **QueryInterface-Methode** der abgerufenen **IUnknown-Schnittstelle** aufrufen, um eine Instanz der [**IWMDRMNonSilentLicenseAquisition-Schnittstelle abzurufen.**](iwmdrmnonsilentlicenseaquisition.md)

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation-Ereignismodells.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Automatischer Lizenzerwerb**](silent-license-acquisition.md)
</dt> </dl>

 

 





