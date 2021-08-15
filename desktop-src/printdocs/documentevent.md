---
description: Die DocumentEvent-Funktion ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: DocumentEvent-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0c38a95c4e0dc9820130e467c971c0adb5b9df0ede248506ed56f963c3246b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971599"
---
# <a name="documentevent-function"></a>DocumentEvent-Funktion

Die **DocumentEvent-Funktion** ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für ein Druckerobjekt. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*hdc* \[ In\]
</dt> <dd>

Ein Gerätekontexthandle, das durch einen Aufruf von [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)generiert wird. Dies ist 0 (null), wenn *iEsc* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt ist. Einschränkungen beim Drucken aus einer 32-Bit-Anwendung in einer 64-Bit-Version von Windows finden Sie unter Hinweise.

</dd> <dt>

*iEsc* 
</dt> <dd>

Ein Escapecode, der das zu behandelnde Ereignis identifiziert. Dieser Parameter kann eine der folgenden ganzzahligen Konstanten sein.



| Konstante                                                                                                                                                                                                                                                                                                                                               | Ereignis                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI ist dabei, einen Aufruf der [**AbortDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) zu verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI hat gerade einen Aufruf der [**CreateDC-**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createica) verarbeitet.<br/> Dieser Escapecode sollte nur verwendet werden, wenn ein vorheriger Aufruf von **DocumentEvent** mit *iEsc* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt wurde.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI ist dabei, einen Aufruf der [**CreateDC-**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createica) zu verarbeiten.<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI ist dabei, einen Aufruf der [**DeleteDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) zu verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI hat gerade einen Aufruf seiner [**EndDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) verarbeitet.<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI ist dabei, einen Aufruf der [**EndDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) zu verarbeiten.<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI ist dabei, einen Aufruf der [**EndPage-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) zu verarbeiten.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | GDI ist dabei, einen Aufruf der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zu verarbeiten.<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Das DOCUMENTEVENT \_ QUERYFILTER-Ereignis stellt eine Gelegenheit für den Spooler dar, den Treiber nach einer Liste der DOCUMENTEVENT \_ *XXX-Ereignisse* abzufragen, auf die der Treiber antwortet. Dieses Ereignis wird unmittelbar vor einem Aufruf von **DocumentEvent** ausgegeben, der das DOCUMENTEVENT \_ CREATEDCPRE-Ereignis übergibt.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI hat gerade einen Aufruf der [**ResetDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) verarbeitet.<br/> Dieser Escapecode sollte nicht verwendet werden, es sei denn, es wurde ein vorheriger Aufruf von **DocumentEvent** mit *iEsc* auf DOCUMENTEVENT \_ RESETDCPRE festgelegt.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI ist dabei, einen Aufruf der [**ResetDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) zu verarbeiten.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI hat gerade einen Aufruf der [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) verarbeitet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI ist dabei, einen Aufruf der [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) zu verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI ist dabei, einen Aufruf seiner [**StartPage-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) zu verarbeiten.<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pvIn* zeigt.

</dd> <dt>

*pvIn* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Was der Puffer enthält, hängt vom Wert von *iEsc* ab, wie in der folgenden Tabelle dargestellt.



| Konstante                                                                                                                                                                                                                                                                                                                                               | pvin-Inhalt                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die im *pvOut-Parameter* in einem vorherigen Aufruf dieser Funktion angegeben wurde, für die der *iEsc-Parameter* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt wurde.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* verweist auf eine DOCEVENT \_ CREATEDCPRE-Struktur, die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | *pvIn* verweist auf eine DOCEVENT \_ ESCAPE-Struktur, die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Identisch mit DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die im *pvOut-Parameter* in einem vorherigen Aufruf dieser Funktion angegeben wurde, für die der *iEsc-Parameter* auf DOCUMENTEVENT \_ RESETDCPRE festgelegt wurde.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die vom Aufrufer von [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)bereitgestellt wird.<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* zeigt auf einen LONG-Wert, der den von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)zurückgegebenen Druckauftragsbezeichner angibt.<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* enthält die Adresse eines Zeigers auf eine [**DOCINFO-Struktur,**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) die vom Aufrufer von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)bereitgestellt wird.<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Wert                       | Bedeutung                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Die Größe des Pufferzeigers auf durch *pvOut* in Bytes.                             |
| DOCUMENTEVENT \_ ESCAPE       | Ein -Wert, der als *cbOutput-Parameter* für [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)verwendet wird. |
| Für alle anderen Werte        | *iEsc* wird nicht verwendet.                                                                  |



 

</dd> <dt>

*pvOut* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Der Inhalt des Puffers hängt vom für *iEsc* angegebenen Wert ab, wie in der folgenden Tabelle dargestellt.



| Konstante                                                                                                                                                                                          | pvOut-Inhalt                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Ein Zeiger auf eine vom Treiber bereitgestellte [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die von GDI anstelle der vom [**CreateDC-Aufrufer**](/windows/desktop/api/wingdi/nf-wingdi-createdca) bereitgestellten Verwendet wird. (Bei **NULL** verwendet GDI die vom Aufrufer bereitgestellte -Struktur.)<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                | Ein Zeiger auf einen Puffer, der als *lpszOutData-Parameter* für [**ExtEscape verwendet wird.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Ein Zeiger auf den Puffer, der eine DOCEVENT FILTER-Struktur enthält, die im Windows \_ Driver Development Kit dokumentiert [ist.](https://msdn.microsoft.com/windows/hardware/gg487428)<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Ein Zeiger auf eine vom Treiber bereitgestellte [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die von GDI anstelle der vom [**ResetDC-Aufrufer bereitgestellten verwendet**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) wird. (Bei **NULL** verwendet GDI die vom Aufrufer bereitgestellte -Struktur.)<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert der Funktion hängt von dem für iEsc bereitgestellten *Escape-Wert ab.* Bei einigen Escapecodes wird der Rückgabewert nicht verwendet (siehe unten). Wenn die Funktion einen Rückgabewert liefert, muss es einer der folgenden sein.



| Rückgabewert               | Bedeutung                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_DOCUMENTEVENT-FEHLER     | Der Treiber unterstützt den von *iEsc* identifizierten Escapecode, aber es ist ein Fehler aufgetreten. |
| DOCUMENTEVENT \_ SUCCESS     | Der Treiber hat den von *iEsc* identifizierten Escapecode erfolgreich verarbeitet.             |
| DOCUMENTEVENT \_ NICHT UNTERSTÜTZT | Der Treiber unterstützt den von *iEsc* identifizierten Escapecode nicht.                 |



 

Die folgende Liste gibt an, welche Escapecodes einen Rückgabewert erfordern und welche nicht, und erläutert die Bedeutung der Rückgabecodes DOCUMENTEVENT \_ SUCCESS, DOCUMENTEVENT FAILURE und \_ DOCUMENTEVENT \_ UNSUPPORTED.



| Rückgabewert                                          | Bedeutung                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | DOCUMENTEVENT FAILURE: GDI erstellt weder den Gerätekontext noch den Informationskontext und stellt den Rückgabewert 0 für \_ [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC zur Verfügung.**](/windows/desktop/api/wingdi/nf-wingdi-createica) |
| DOCUMENTEVENT \_ DELETEDC                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC     | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ESCAPE                                 | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Siehe Hinweise.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | DOCUMENTEVENT FAILURE: GDI setzt den Gerätekontext nicht zurück und gibt den Rückgabewert 0 für \_ [**ResetDC an.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | DOCUMENTEVENT \_ FAILURE : GDI ruft [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) auf, um das Dokument zu beenden, und gibt dann den Rückgabewert SP \_ ERROR für [**StartDoc an.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)                      |
| DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC | DOCUMENTEVENT FAILURE : GDI startet das Dokument nicht und gibt den Rückgabewert \_ SP \_ ERROR für [**StartDoc an.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | DOCUMENTEVENT FAILURE : GDI startet die Seite nicht und gibt den Rückgabewert \_ SP \_ ERROR für [**StartPage an.**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)                                                         |



 

## <a name="remarks"></a>Hinweise

Bei *einem iEsc-Wert* von DOCUMENTEVENT QUERYFILTER kann der Spooler einen von DocumentEvent zurückgegebenen DOCUMENTEVENT SUCCESS-Wert auf zwei Arten interpretieren, je nachdem, ob der Treiber bestimmte Elemente der DOCEVENT FILTER-Struktur geändert hat (dies ist im \_ Windows Driver Development \_  \_ [Kit](https://msdn.microsoft.com/windows/hardware/gg487428) dokumentiert). (Der *pvOut-Parameter* verweist auf diese Struktur.) Wenn der Spooler Speicher für eine Struktur dieses Typs zuteilen, initialisiert er zwei Member dieser Struktur, **cElementsReturned** und **cElementsNeeded,** für bekannte Werte. Nachdem **DocumentEvent** zurückgegeben wurde, bestimmt der Spooler, ob sich die Werte dieser Member geändert haben, und verwendet diese Informationen, um den **DocumentEvent-Rückgabewert** zu interpretieren. In der folgenden Tabelle wird diese Situation zusammengefasst.



| Rückgabewert                          | Status von cElementsReturned und cElementsNeeded    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ SUCCESS<br/>     | Der Treiber hat keine Änderung an beiden Membern vorgenommen.<br/> | Der Spooler interpretiert diesen Rückgabewert als äquivalent zu DOCUMENTEVENT \_ UNSUPPORTED. Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er beim Aufrufen von **DocumentEvent** für alle Ereignisse beibehalten wird.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ SUCCESS<br/>     | Der Treiber hat in einen oder beide Member geschrieben.<br/>    | Der Spooler akzeptiert diesen Rückgabewert ohne Interpretation. Wenn der Treiber nur in eines von **cElementsNeeded** und **cElementsReturned** geschrieben hat, betrachtet der Spooler das unveränderte Element als wert 0 (null).<br/> Der Spooler filtert alle Ereignisse heraus, die im **aDocEventCall-Mitglied** von DOCEVENT FILTER aufgeführt sind (dies ist im \_ Windows Driver Development Kit [dokumentiert).](https://msdn.microsoft.com/windows/hardware/gg487428)<br/> |
| DOCUMENTEVENT \_ NICHT UNTERSTÜTZT<br/> | Nicht verfügbar<br/>                          | Der Treiber unterstützt DOCUMENTEVENT \_ QUERYFILTER nicht.<br/> Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er beim Aufrufen von **DocumentEvent** für alle Ereignisse beibehalten wird.<br/>                                                                                                                                                                                                                                            |
| \_DOCUMENTEVENT-FEHLER<br/>     | Nicht verfügbar<br/>                          | Der Treiber unterstützt DOCUMENTEVENT \_ QUERYFILTER, aber es ist ein interner Fehler aufgetreten.<br/> Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er beim Aufrufen von **DocumentEvent** für alle Ereignisse beibehalten wird.<br/>                                                                                                                                                                                                                 |



 

Wenn der im *iEsc-Parameter* angegebene Escapecode DOCUMENTEVENT \_ CREATEDCPRE ist, gelten die folgenden Regeln:

-   Wenn der Auftrag ohne Spooling direkt an den Drucker gesendet wird, verweist pvIn->pszDevice auf den Druckernamen. (Weitere Informationen finden Sie in der Dokumentation zu DOCEVENT. \_ CREATEDCPRE-Struktur im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).)
-   Wenn der Auftrag in einen Pool poolt wird, zeigt pvIn->pszDevice auf den Druckerportnamen.

> [!Note]  
> Die folgenden Einschränkungen gelten beim Ausführen einer 32-Bit-Anwendung auf einer 64-Bit-Version Windows. Die einzige GDI-Funktion, **die DocumentEvent** aufrufen sollte, ist [**ExtEscape,**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)und es sollten nur private Escapes verwendet werden. **DocumentEvent-Aufrufe** anderer GDI-Funktionen können zu nicht definiertem Verhalten führen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DocumentEventW** (Unicode) und **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

