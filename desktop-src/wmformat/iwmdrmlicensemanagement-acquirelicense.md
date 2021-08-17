---
title: IWMDRMLicenseManagement AcquireLicense-Methode (Wmdrmsdk.h)
description: Die AcquireLicense-Methode ruft asynchron eine Lizenz von einer angegebenen URL ab.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- AcquireLicense-Methode windows Media Format
- AcquireLicense-Methode windows Media Format , IWMDRMLicenseManagement-Schnittstelle
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

Die **AcquireLicense-Methode** ruft asynchron eine Lizenz von einer angegebenen URL ab.

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

URL des Lizenzservers, von dem die Lizenz erworben werden soll. Übergeben Sie **NULL,** damit die -Methode die URL aus dem Inhaltsheader analysiert.

</dd> <dt>

*bstrHeaderData* \[ In\]
</dt> <dd>

Inhaltsheader, der an den Lizenzserver übergeben werden soll. Wenn *bstrURL* **NULL** ist, analysiert die Methode die URL aus diesem Header. Wenn *dwFlags* auf WMDRM \_ ACQUIRE LICENSE LEGACY \_ \_ \_ NONSILENT festgelegt ist, legen Sie diesen Wert auf die Schlüssel-ID anstelle des gesamten Inhaltsheaders fest.

</dd> <dt>

*bstrActions* \[ In\]
</dt> <dd>

Zeichenfolge, die 0 (null) oder mehr Aktionen enthält, für die die Berechtigung in der Lizenz angefordert werden soll. Die Zeichenfolge muss wie folgt formatiert werden:

-   Jede Aktion muss innerhalb eines ACTION-Elements definiert werden. Die Daten des Elements sind die Aktionszeichenfolge.
-   Alle ACTION-Elemente müssen in einem ACTIONLIST-Element enthalten sein.

    Die Zeichenfolge zum Anfordern einer Lizenz zum Wiedergeben von Inhalten ist beispielsweise wie folgt formatiert:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Lizenzerwerbsoptionsflags. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| Konstante                                   | Beschreibung                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ – LIZENZ IM \_ HINTERGRUND ERWERBEN \_            | Die Lizenz wird ohne Bestätigung durch die Clientanwendung direkt über das Internet ausgestellt.              |
| WMDRM \_ – \_ LIZENZ \_ NICHTSILENT ERWERBEN         | Das DRM-Subsystem erstellt eine Lizenzanforderung, die asynchron für die Bereitstellung an den Lizenzserver zurückgegeben wird. |
| WMDRM \_ ACQUIRE \_ LICENSE \_ LEGACY \_ NONSILENT | Identisch mit WMDRM \_ ACQUIRE \_ LICENSE \_ NONSILENT, mit der Ausnahme, dass eine DRM-Lizenzaufforderung der Version 1 erstellt wird.           |



 

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



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Er gibt sofort nach dem Aufruf zurück und generiert dann ein **MEWMDRMLicenseAcquisitionCompleted-Ereignis,** wenn die Verarbeitung abgeschlossen ist. Bei Nicht-unbeaufsichtigten Lizenzerwerbsvorgängen ist der Wert des Ereignisses, das durch Aufrufen von **POINTERMediaEvent::GetValue** abgerufen wird, ein **IUnknown-Zeiger.** Sie können die **QueryInterface-Methode** der abgerufenen **IUnknown-Schnittstelle** aufrufen, um eine Instanz der [**IWMDRMNonSilentLicenseAquisition-Schnittstelle**](iwmdrmnonsilentlicenseaquisition.md) abzurufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation Ereignismodells.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Unbeaufsichtigter Lizenzerwerb**](silent-license-acquisition.md)
</dt> </dl>

 

 





