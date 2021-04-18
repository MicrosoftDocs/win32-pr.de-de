---
description: Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Iwiaerrorhandler:: Report Status-Methode (WIA. h)'
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
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357770"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>Iwiaerrorhandler:: Report Status-Methode

Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.

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

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

**HWND** , das das übergeordnete Fenster für das Nachrichtenfenster ist.

</dd> <dt>

*punkitem* \[ in\]
</dt> <dd>

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ein Zeiger auf die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des übertragenen Elements. Dieses Objekt implementiert mindestens [_ *IWiaItem2* *](-wia-iwiaitem2.md) und [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Typ: **HRESULT**

**HRESULT** , das der von [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangene Statuscode ist.

</dd> <dt>

*cbreslength* \[ in\]
</dt> <dd>

Type: **Long**

**Long** , d. h. die Größe der Daten, auf die von *pbData* verwiesen wird.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Zeiger auf den Datenpuffer, wie von [_ *banbeddatacallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt *hrStatus* zurück, wenn der Fehler nicht von wieder hergestellt werden kann. Andernfalls wird einer der folgenden Werte zurückgegeben.



| Rückgabecode                                                                             | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die entsprechende Aktion wurde durchgeführt, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden. <br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Es wurde keine Aktion zum Behandeln des Fehlers oder zum Melden des Status für den Benutzer ausgeführt. <br/>                |
| <dl> <dt>**E \_ Abbrechen**</dt> </dl> | Der Benutzer hat die Übertragung als Reaktion auf das angezeigte Dialogfeld abgebrochen. <br/>        |



 

## <a name="remarks"></a>Bemerkungen

Windows-Abbild Beschaffung (WIA) 2,0 ruft **iwiaerrorhandler:: Report Status** auf, wenn der Treiber eine IT-Nachrichten **\_ \_ Geräte \_ Status** Meldung an [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)sendet. Diese Methode verarbeitet die Nachricht und zeigt dem Benutzerinformationen zum Status oder Fehler an. Wenn es sich bei der Nachricht um einen Fehler handelt, kann der Benutzer die Methode nach Möglichkeit auswählen, ob versucht werden soll, den Fehler zu beheben und die Übertragung fortzusetzen oder abzubrechen.

*hrStatus* ist auf WIA \_ Status \_ Transfer BEGIN festgelegt \_ , um den Handler darüber zu informieren, dass eine Übertragung gestartet wurde. \_ \_ \_ Wenn die Übertragung abgeschlossen ist, wird Sie auf das Ende der Status Übertragung festgelegt.

Wenn *hrStatus* den Schweregrad \_ Success hat, sollte der Benutzer die Übertragung abbrechen dürfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
