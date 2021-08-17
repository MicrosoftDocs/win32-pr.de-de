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

Ein Handle für ein Druckerobjekt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*hdc* \[ In\]
</dt> <dd>

Ein Gerätekontexthand handle, das durch einen Aufruf von [**CreateDC generiert wird.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) Dies ist 0 *(null), wenn iEsc* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt ist. Einschränkungen für das Drucken aus einer 32-Bit-Anwendung in einer 64-Bit-Version von Windows sie unter Hinweise.

</dd> <dt>

*iEsc* 
</dt> <dd>

Ein Escapecode, der das zu behandelnde Ereignis identifiziert. Dieser Parameter kann eine der folgenden ganzzahligen Konstanten sein.



| Konstante                                                                                                                                                                                                                                                                                                                                               | Ereignis                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI wird einen Aufruf seiner [**AbortDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI hat gerade einen Aufruf seiner [**CreateDC-**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createica) verarbeitet.<br/> Dieser Escapecode sollte nur verwendet werden, wenn ein vorheriger Aufruf von **DocumentEvent** mit *iEsc* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt wurde.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI wird einen Aufruf seiner [**CreateDC-**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createica) verarbeiten.<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI ist dabei, einen Aufruf seiner [**DeleteDC-Funktion zu**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI hat gerade einen Aufruf seiner [**EndDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) verarbeitet.<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI wird einen Aufruf seiner [**EndDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) verarbeiten.<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI wird einen Aufruf seiner [**EndPage-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) verarbeiten.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | GDI wird einen Aufruf seiner [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) verarbeiten.<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Das DOCUMENTEVENT QUERYFILTER-Ereignis stellt eine Möglichkeit für den Spooler dar, den Treiber nach einer Liste der \_ DOCUMENTEVENT \_ *XXX-Ereignisse* abfragt, auf die der Treiber reagiert. Dieses Ereignis wird direkt vor einem Aufruf von **DocumentEvent** ausgegeben, der das DOCUMENTEVENT \_ CREATEDCPRE-Ereignis übergibt.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI hat gerade einen Aufruf seiner [**ResetDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) verarbeitet.<br/> Dieser Escapecode sollte nur verwendet werden, wenn ein vorheriger Aufruf von **DocumentEvent** mit *iEsc* auf DOCUMENTEVENT \_ RESETDCPRE festgelegt wurde.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI wird einen Aufruf seiner [**ResetDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) verarbeiten.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI hat gerade einen Aufruf seiner [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) verarbeitet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI wird einen Aufruf seiner [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) verarbeiten.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI wird einen Aufruf seiner [**StartPage-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) verarbeiten.<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pvIn zeigt.*

</dd> <dt>

*pvIn* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Was der Puffer enthält, hängt vom Wert von *iEsc* ab, wie in der folgenden Tabelle gezeigt.



| Konstante                                                                                                                                                                                                                                                                                                                                               | pvin-Inhalt                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die im *pvOut-Parameter* in einem vorherigen Aufruf dieser Funktion angegeben wurde, für die der *iEsc-Parameter* auf DOCUMENTEVENT \_ CREATEDCPRE festgelegt wurde.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* verweist auf eine DOCEVENT \_ CREATEDCPRE-Struktur, die im Windows [Driver Development Kit dokumentiert ist.](https://msdn.microsoft.com/windows/hardware/gg487428)<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | *pvIn* verweist auf eine DOCEVENT \_ ESCAPE-Struktur, die im Windows [Driver Development Kit dokumentiert ist.](https://msdn.microsoft.com/windows/hardware/gg487428)<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Identisch mit documentevent \_ createdcpre.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die im *pvOut-Parameter* in einem vorherigen Aufruf dieser Funktion angegeben wurde, für die der *iEsc-Parameter* auf DOCUMENTEVENT \_ RESETDCPRE festgelegt wurde.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* enthält die Adresse eines Zeigers auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die vom Aufrufer von [**ResetDC bereitgestellt wird.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* zeigt auf einen LONG-Wert, der den von StartDoc zurückgegebenen [**Druckauftragsbezeichner angibt.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* enthält die Adresse eines Zeigers auf eine [**DOCINFO-Struktur,**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) die vom Aufrufer von [**StartDoc bereitgestellt wird.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | Wird nicht verwendet.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Wert                       | Bedeutung                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Die Größe des Pufferzeigers auf durch pvOut in *Bytes.*                             |
| DOCUMENTEVENT \_ ESCAPE       | Ein -Wert, der als *cbOutput-Parameter* für [**ExtEscape verwendet wird.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) |
| Für alle anderen Werte        | *iEsc* wird nicht verwendet.                                                                  |



 

</dd> <dt>

*pvOut* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Der Inhalt des Puffers hängt von dem für *iEsc* angegebenen Wert ab, wie in der folgenden Tabelle gezeigt.



| Konstante                                                                                                                                                                                          | pvOut-Inhalt                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Ein Zeiger auf eine vom Treiber bereitgestellte [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die von GDI anstelle der vom [**CreateDC-Aufrufer bereitgestellten verwendet**](/windows/desktop/api/wingdi/nf-wingdi-createdca) wird. (Bei **NULL** verwendet GDI die vom Aufrufer bereitgestellte Struktur.)<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                | Ein Zeiger auf einen Puffer, der als *lpszOutData-Parameter* für [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)verwendet wird.<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Ein Zeiger auf den Puffer, der eine DOCEVENT \_ FILTER-Struktur enthält, die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Ein Zeiger auf eine vom Treiber bereitgestellte [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die von GDI anstelle der vom [**ResetDC-Aufrufer**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) bereitgestellten Verwendet wird. (Bei **NULL** verwendet GDI die vom Aufrufer bereitgestellte Struktur.)<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert der Funktion ist von dem für *iEsc* bereitgestellten Escapewert abhängig. Bei einigen Escapecodes wird der Rückgabewert nicht verwendet (siehe unten). Wenn die Funktion einen Rückgabewert angibt, muss es sich um einen der folgenden Werte handelt.



| Rückgabewert               | Bedeutung                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_DOCUMENTEVENT-FEHLER     | Der Treiber unterstützt den von *iEsc* identifizierten Escapecode, aber es ist ein Fehler aufgetreten. |
| DOCUMENTEVENT \_ SUCCESS     | Der Treiber hat den von *iEsc* identifizierten Escapecode erfolgreich verarbeitet.             |
| DOCUMENTEVENT \_ NICHT UNTERSTÜTZT | Der Treiber unterstützt den von *iEsc* identifizierten Escapecode nicht.                 |



 

Die folgende Liste gibt an, welche Escapecodes einen Rückgabewert erfordern und welche nicht. Außerdem wird die Bedeutung der Rückgabecodes DOCUMENTEVENT \_ SUCCESS, DOCUMENTEVENT \_ FAILURE und DOCUMENTEVENT \_ UNSUPPORTED erläutert.



| Rückgabewert                                          | Bedeutung                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | DOCUMENTEVENT \_ FAILURE: GDI erstellt keinen Gerätekontext oder Informationskontext und stellt den Rückgabewert 0 für [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**CreateIC bereit.**](/windows/desktop/api/wingdi/nf-wingdi-createica) |
| DOCUMENTEVENT \_ DELETEDC                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE oder DOCUMENTEVENT \_ ENDDOC     | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ ESCAPE                                 | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Siehe Hinweise.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | DOCUMENTEVENT \_ FAILURE : GDI setzt den Gerätekontext nicht zurück und stellt den Rückgabewert 0 für [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)bereit.                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | DOCUMENTEVENT \_ FAILURE : GDI ruft [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) auf, um das Dokument zu beenden, und stellt dann den Rückgabewert SP \_ ERROR für [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)bereit.                      |
| DOCUMENTEVENT \_ STARTDOCPRE oder DOCUMENTEVENT \_ STARTDOC | DOCUMENTEVENT \_ FAILURE : GDI startet das Dokument nicht und stellt den Rückgabewert SP \_ ERROR für [**StartDoc bereit.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | DOCUMENTEVENT \_ FAILURE : GDI startet die Seite nicht und stellt den Rückgabewert SP \_ ERROR für [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)bereit.                                                         |



 

## <a name="remarks"></a>Hinweise

Bei einem *iEsc-Wert* von DOCUMENTEVENT \_ QUERYFILTER kann der Spooler einen von \_ **DocumentEvent** zurückgegebenen DOCUMENTEVENT SUCCESS-Wert auf zwei Arten interpretieren, je nachdem, ob der Treiber bestimmte Member der DOCEVENT FILTER-Struktur geändert hat \_ (dies ist im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) dokumentiert). (Der *pvOut-Parameter* zeigt auf diese Struktur.) Wenn der Spooler Speicher für eine Struktur dieses Typs zuordnet, initialisiert er zwei Member dieser Struktur, **cElementsReturned** und **cElementsNeeded,** mit bekannten Werten. Nachdem **DocumentEvent** zurückgegeben wurde, bestimmt der Spooler, ob sich die Werte dieser Member geändert haben, und verwendet diese Informationen, um den **DocumentEvent-Rückgabewert** zu interpretieren. In der folgenden Tabelle ist diese Situation zusammengefasst.



| Rückgabewert                          | Status von cElementsReturned und cElementsNeeded    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ SUCCESS<br/>     | Der Treiber hat keine Änderungen an beiden Membern vorgenommen.<br/> | Der Spooler interpretiert diesen Rückgabewert als äquivalent zu DOCUMENTEVENT \_ UNSUPPORTED. Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er **documentEvent** für alle Ereignisse weiterhin aufruft.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ SUCCESS<br/>     | Der Treiber hat in einen oder beide Member geschrieben.<br/>    | Der Spooler akzeptiert diesen Rückgabewert ohne Interpretation. Wenn der Treiber nur in eines von **cElementsNeeded** und **cElementsReturned** geschrieben hat, betrachtet der Spooler den unveränderten Member als den Wert 0 (null).<br/> Der Spooler filtert alle Ereignisse heraus, die im **aDocEventCall-Element** von DOCEVENT FILTER aufgeführt sind \_ (dies ist im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) dokumentiert).<br/> |
| DOCUMENTEVENT \_ NICHT UNTERSTÜTZT<br/> | Nicht verfügbar<br/>                          | Der Treiber unterstützt DOCUMENTEVENT \_ QUERYFILTER nicht.<br/> Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er **documentEvent** für alle Ereignisse weiterhin aufruft.<br/>                                                                                                                                                                                                                                            |
| \_DOCUMENTEVENT-FEHLER<br/>     | Nicht verfügbar<br/>                          | Der Treiber unterstützt DOCUMENTEVENT \_ QUERYFILTER, es ist jedoch ein interner Fehler aufgetreten.<br/> Der Spooler kann den Ereignisfilter nicht vom Treiber abrufen, sodass er **documentEvent** für alle Ereignisse weiterhin aufruft.<br/>                                                                                                                                                                                                                 |



 

Wenn der im *iEsc-Parameter* angegebene Escapecode DOCUMENTEVENT \_ CREATEDCPRE ist, gelten die folgenden Regeln:

-   Wenn der Auftrag ohne Spooling direkt an den Drucker gesendet wird, verweist pvIn->pszDevice auf den Druckernamen. (Weitere Informationen finden Sie in der Dokumentation zu DOCEVENT. \_ CREATEDCPRE-Struktur im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).)
-   Wenn der Auftrag gepoolt wird, verweist pvIn->pszDevice auf den Namen des Druckerports.

> [!Note]  
> Die folgenden Einschränkungen gelten beim Ausführen einer 32-Bit-Anwendung auf einer 64-Bit-Version von Windows. Die einzige GDI-Funktion, die **DocumentEvent** aufrufen soll, ist [**ExtEscape,**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)und es sollten nur private Escapes verwendet werden. **DocumentEvent-Aufrufe** anderer GDI-Funktionen können zu undefiniertem Verhalten führen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
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

 

