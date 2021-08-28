---
description: Behandelt Status- und Fehlermeldungen während Bilddatenübertragungen und zeigt sie dem Benutzer an.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: IWiaErrorHandler::ReportStatus-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6604dc8dbf0cad5f31449ff3cc30945c1e6059727d513fa98dbf436eb199f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659750"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>IWiaErrorHandler::ReportStatus-Methode

Behandelt Status- und Fehlermeldungen während Bilddatenübertragungen und zeigt sie dem Benutzer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

**HWND,** das das übergeordnete Fenster für das Meldungsfenster ist.

</dd> <dt>

*-Item* \[ In\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Zeiger auf die [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) des elements, das übertragen wird. Dieses Objekt implementiert [**IWiaItem2**](-wia-iwiaitem2.md) und [**IWiaDataTransfer minimal.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)

</dd> <dt>

*hrStatus* \[ In\]
</dt> <dd>

Typ: **HRESULT**

**HRESULT,** bei dem es sich um den Statuscode handelt, der von [**BandedDataCallback empfangen wird.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ In\]
</dt> <dd>

Typ: **LONG**

**LONG,** das die Größe der Daten ist, auf die von *pbData verwiesen wird.*

</dd> <dt>

*pbData* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Zeiger auf den Datenpuffer, der von [**BandedDataCallback empfangen wird.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt *hrStatus zurück,* wenn der Fehler nicht wiederhergestellt werden kann. Andernfalls wird einer der folgenden Werte zurückgegeben.



| Rückgabecode                                                                             | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die entsprechende Aktion wurde ergriffen, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden. <br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Es wurde keine Aktion ergriffen, um den Fehler zu behandeln oder dem Benutzer den Status zu melden. <br/>                |
| <dl> <dt>**E \_ ABORT**</dt> </dl> | Der Benutzer hat die Übertragung als Reaktion auf das angezeigte Dialogfeld abgebrochen. <br/>        |



 

## <a name="remarks"></a>Hinweise

Windows Image Acquisition (WIA) 2.0 ruft **IWiaErrorHandler::ReportStatus** auf, wenn der Treiber eine **IT \_ MSG \_ DEVICE \_ STATUS-Meldung** an [**BandedDataCallback sendet.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback) Diese Methode verarbeitet die Meldung und zeigt dem Benutzer Informationen zum Status oder Fehler an. Wenn es sich bei der Meldung um einen Fehler handelt, kann der Benutzer mit der -Methode nach Möglichkeit auswählen, ob nach dem Fehler eine Wiederherstellung versucht und die Übertragung fortgesetzt oder abgebrochen werden soll.

*hrStatus* ist auf WIA STATUS TRANSFER BEGIN festgelegt, um den Handler zu informieren, \_ dass eine Übertragung gestartet \_ \_ wurde. Sie wird auf WIA \_ STATUS \_ TRANSFER END \_ festgelegt, wenn die Übertragung abgeschlossen ist.

Wenn *hrStatus* den Schweregrad ERFOLG hat, sollte der Benutzer \_ die Übertragung abbrechen dürfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
