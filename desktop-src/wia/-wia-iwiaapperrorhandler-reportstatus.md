---
description: Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Iwiaapperrorhandler:: Report Status-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356532"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>Iwiaapperrorhandler:: Report Status-Methode

Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*pWiaItem2* \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Zeiger auf das Element, das übertragen wird.

</dd> <dt>

_hrStatus * \[ in\]
</dt> <dd>

Typ: **HRESULT**

Gerätestatus Code.

</dd> <dt>

*lprozentuabgeschlossen* \[ in\]
</dt> <dd>

Type: **Long**

Der Prozentsatz des aktuellen Vorgangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt " *hrStatus* " zurück, wenn die Wiederherstellung nach dem Fehler nicht möglich ist. Andernfalls wird einer der folgenden Werte zurückgegeben.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Wenn *hrStatus* ein Fehler ist, wurde die entsprechende Aktion ausgeführt, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden. Wenn *hrStatus* Information lautet, wurde der Benutzer über ein nicht modalem Dialogfeld informiert, und die Übertragung konnte nicht abgebrochen werden.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                  | Der Benutzer hat die Übertragung aus dem Dialogfeld "Fehlerhandler-nicht modelliert" abgebrochen. Dieser Wert kann jederzeit unabhängig von *hrStatus* zurückgegeben werden. <br/>                                                                                      |
| <dl> <dt>**WIA- \_ Status \_ nicht \_ behandelt**</dt> </dl> | Es wurde keine Aktion ausgeführt. Das heißt, dem Benutzer wurde kein Dialogfeld angezeigt. Der nächste Fehlerhandler wird aufgerufen. Die Reihenfolge von Fehler Handlern lautet: Anwendung, Treiber und System Standard.<br/>                                                 |



 

## <a name="remarks"></a>Bemerkungen

Der *lprozentucomplete* -Parameter ermöglicht einem fehlerhandlerfenster, den Fortschritt anzuzeigen. Ein Treiber könnte z. b. eine Schätzung der Dauer der "Aufwärm Dauer" bereitstellen. Der an **iwiaapperrorhandler:: Report Status** übergebenen *lprozentucomplete* -Parameter ist derselbe Wert wie der **lprozentucomplete** , den der Treiber in der [**wiatransferparameams**](-wia-wiatransferparams.md) -Struktur festlegt.

Ein Fehlerhandler kann die Makros "erfolgreich" und "fehlgeschlagen" verwenden, um herauszufinden, ob " *hrStatus* " einen Schweregrad \_ oder einen Schweregrad " \_

Wenn *hrStatus* den Schweregrad \_ Success hat, sollte der Benutzer die Übertragung abbrechen dürfen.

Wenn für *hrStatus* der Schweregrad \_ Fehler vorliegt, sollte der Fehlerhandler ein modales Dialogfeld im Besitz des übergeordneten Fensters der Anwendung anzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




