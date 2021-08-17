---
description: Behandelt Gerätestatus- und Fehlermeldungen während Bilddatenübertragungen und zeigt die Meldungen dem Benutzer an.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: IWiaAppErrorHandler::ReportStatus-Methode (Wia.h)
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
ms.openlocfilehash: 9cc727845489740fae54dcc96bf5bc903bceb0205688c1c60bee3df980f66845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965749"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>IWiaAppErrorHandler::ReportStatus-Methode

Behandelt Gerätestatus- und Fehlermeldungen während Bilddatenübertragungen und zeigt die Meldungen dem Benutzer an.

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*pWiaItem2* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Zeiger auf das element, das übertragen wird.

</dd> <dt>

*hrStatus* \[ In\]
</dt> <dd>

Typ: **HRESULT**

Gerätestatuscode.

</dd> <dt>

*lPercentComplete* \[ In\]
</dt> <dd>

Typ: **LONG**

Prozentsatz des abschlusses des aktuellen Vorgangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt *hrStatus* zurück, wenn die Wiederherstellung nach dem Fehler nicht möglich ist. Andernfalls wird einer der folgenden Werte zurückgegeben.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Wenn *hrStatus* ein Fehler ist, wurde die entsprechende Aktion ausgeführt, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden. Wenn *hrStatus* informational ist, wurde der Benutzer mit einem moduslosen Dialogfeld informiert und hat sich entschieden, die Übertragung nicht abzubrechen.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                  | Der Benutzer hat die Übertragung über das Dialogfeld "Fehlerhandlermoduslos" abgebrochen. Dieser Wert kann jederzeit zurückgegeben werden, unabhängig davon, was *hrStatus* ist. <br/>                                                                                      |
| <dl> <dt>**\_WIA-STATUS \_ NICHT \_ BEHANDELT**</dt> </dl> | Es wurde keine Aktion ausgeführt. Das heißt, dem Benutzer wurde kein Dialogfeld angezeigt. Der nächste Fehlerhandler wird aufgerufen. Die Reihenfolge der Fehlerhandler lautet: Anwendungs-, Treiber- und Systemstandard.<br/>                                                 |



 

## <a name="remarks"></a>Hinweise

Mit dem *Parameter lPercentComplete* kann ein Fehlerhandlerfenster den Fortschritt anzeigen. Beispielsweise kann ein Fahrer eine Schätzung angeben, wie lange die "Aufwärmdauer" dauert. Der *lPercentComplete-Parameter,* der an **IWiaAppErrorHandler::ReportStatus** übergeben wird, ist der gleiche Wert wie der **lPercentComplete,** den der Treiber in die [**WiaTransferParams-Struktur**](-wia-wiatransferparams.md) festlegt.

Ein Fehlerhandler kann die Makros SUCCEEDED und FAILED verwenden, um zu ermitteln, ob *hrStatus* den Schweregrad SEVERITY \_ ERROR oder SEVERITY \_ SUCCESS aufweist.

Wenn *hrStatus* auf SEVERITY SUCCESS festgelegt \_ ist, sollte der Benutzer berechtigt sein, die Übertragung abzubrechen.

Wenn *hrStatus* den Status SEVERITY ERROR \_ aufweist, sollte der Fehlerhandler ein modales Dialogfeld anzeigen, das sich im Besitz des übergeordneten Fensters der Anwendung befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




