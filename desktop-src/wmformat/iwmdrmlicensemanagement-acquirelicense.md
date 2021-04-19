---
title: Iwmdrmlicenabmanagement AcquireLicense-Methode (wmdrmsdk. h)
description: Die AcquireLicense-Methode ruft asynchron eine Lizenz von einer angegebenen URL ab.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- AcquireLicense-Methode, Windows Media-Format
- AcquireLicense-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement-Schnittstelle Windows Media-Format, AcquireLicense-Methode
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
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352959"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>Iwmdrmlicenabmanagement:: AcquireLicense-Methode

Die **AcquireLicense** -Methode ruft asynchron eine Lizenz von einer angegebenen URL ab.

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

*bstrinurl* \[ in\]
</dt> <dd>

Die URL des Lizenzservers, von dem die Lizenz abgerufen werden soll. Übergeben Sie **null** , damit die-Methode die URL aus dem Content-Header analysieren muss.

</dd> <dt>

*bstrinheaderdata* \[ in\]
</dt> <dd>

Inhalts Header, der an den Lizenzserver übermittelt werden soll. Wenn *bstrinurl* **null** ist, analysiert die Methode die URL aus diesem Header. Wenn *dwFlags* auf WMDRM-Lizenz "Legacy" für "nicht unbeaufsichtigt" festlegen festgelegt ist \_ \_ \_ \_ , legen Sie diesen Wert auf die Schlüssel-ID anstelle des gesamten Inhalts Headers fest.

</dd> <dt>

*bstractions* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die NULL oder mehr Aktionen enthält, für die die Berechtigung in der Lizenz angefordert werden soll. Die Zeichenfolge muss wie folgt formatiert werden:

-   Jede Aktion muss innerhalb eines Action-Elements definiert werden. Die Daten des Elements sind die Aktions Zeichenfolge.
-   Alle Aktions Elemente müssen in einem Action list-Element enthalten sein.

    Beispielsweise wird die Zeichenfolge zum Anfordern einer Lizenz für die Wiedergabe von Inhalten wie folgt formatiert:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Options Flags für die Lizenz Beschaffung. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| Konstante                                   | BESCHREIBUNG                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM-Lizenz wird automatisch abgerufen \_ \_ \_            | Die Lizenz wird ohne Bestätigung durch die Client Anwendung direkt über das Internet ausgestellt.              |
| WMDRM \_ - \_ Lizenz \_ nicht unbeaufsichtigt erwerben         | Das DRM-Subsystem erstellt eine Lizenz Anforderung, die asynchron für die Bereitstellung auf dem Lizenzserver zurückgegeben wird. |
| WMDRM \_ - \_ Lizenz für \_ ältere Lizenz \_ | Identisch mit der WMDRM \_ - \_ \_ Erstellungs Lizenz, mit der Ausnahme, dass eine Lizenz Herausforderung der DRM-Version 1 erstellt wird.           |



 

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

Diese Methode wird asynchron ausgeführt. Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann ein **mewmdrmlicenabacquisitioncomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist. Bei nicht automatischen Lizenz Erwerbs Vorgängen ist der Wert des Ereignisses, das durch den Aufruf von **imfmediaevent:: GetValue** abgerufen wurde, ein **IUnknown** -Zeiger. Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle abrufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Automatische Lizenz Beschaffung**](silent-license-acquisition.md)
</dt> </dl>

 

 





