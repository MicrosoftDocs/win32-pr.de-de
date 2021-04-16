---
description: Die DocumentEvent-Funktion ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: DocumentEvent-Funktion (winspool. h)
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
ms.openlocfilehash: aa80e5fe17047eceacdc30e2a40a4a629088d89f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529009"
---
# <a name="documentevent-function"></a>DocumentEvent-Funktion

Die **DocumentEvent** -Funktion ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für ein Drucker Objekt. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*hdc* \[ in\]
</dt> <dd>

Ein Gerätekontext handle, das durch einen-Befehl von " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca)" generiert wird. Dieser Wert ist 0 (null), wenn *IESC* auf DocumentEvent \_ kreatedcpre festgelegt ist. Informationen zu Einschränkungen beim Drucken aus einer 32-Bit-Anwendung in einer 64-Bit-Version von Windows finden Sie unter "Hinweise".

</dd> <dt>

*IESC* 
</dt> <dd>

Ein Escapecode, der das Ereignis identifiziert, das behandelt werden soll. Dieser Parameter kann eine der folgenden ganzzahligen Konstanten sein.



| Konstante                                                                                                                                                                                                                                                                                                                                               | Ereignis                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DocumentEvent \_ abortdoc**</dt> </dl>                                                                                                                                                               | GDI verarbeitet einen Aufrufvorgang der [**abortdoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) -Funktion.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DocumentEvent | \_ atedcpost**</dt> </dl>                                                                                                                                                   | GDI hat soeben einen aufzurufenden Befehl an die Funktion " [**inatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) " oder " [**inateic**](/windows/desktop/api/wingdi/nf-wingdi-createica) " verarbeitet.<br/> Dieser Escapecode sollte nicht verwendet werden, es sei denn, es wurde ein vorheriger **DocumentEvent** -Befehl mit *IESC* auf DocumentEvent | \_ atedcpre festgelegt.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DocumentEvent | \_ atedcpre**</dt> </dl>                                                                                                                                                      | GDI verarbeitet einen aufzurufenden Rückruf der Funktion " [**inatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) " oder " [**inateic**](/windows/desktop/api/wingdi/nf-wingdi-createica) ".<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DocumentEvent \_ DeleteDC**</dt> </dl>                                                                                                                                                               | GDI verarbeitet einen Aufrufvorgang der [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) -Funktion.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DocumentEvent \_ enddocpost**</dt> </dl>                                                                                                                                                         | GDI hat soeben einen aufzurufenden [**Endpunkt der EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) -Funktion verarbeitet.<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DocumentEvent \_ enddocpre oder DocumentEvent \_ EndDoc**</dt> </dl>                 | GDI verarbeitet einen Aufrufvorgang der [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) -Funktion.<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DocumentEvent- \_ EndPage**</dt> </dl>                                                                                                                                                                  | GDI soll einen Aufrufvorgang der [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) -Funktion verarbeiten.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DocumentEvent-Escapezeichen \_**</dt> </dl>                                                                                                                                                                     | GDI soll einen Aufrufvorgang der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion verarbeiten.<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DocumentEvent- \_ QueryFilter**</dt> </dl>                                                                                                                                                      | Das DocumentEvent \_ QueryFilter-Ereignis stellt eine Möglichkeit für den Spooler dar, den Treiber nach einer Liste der DocumentEvent \_ *xxx* -Ereignisse abzufragen, auf die der Treiber antwortet. Dieses Ereignis wird unmittelbar vor dem Aufrufen von **DocumentEvent** ausgegeben, das das DocumentEvent- \_ Ereignis "| atedcpre" übergibt.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DocumentEvent \_ resetdcpost**</dt> </dl>                                                                                                                                                      | GDI hat soeben einen Aufrufen der [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) -Funktion verarbeitet.<br/> Dieser Escapecode sollte nicht verwendet werden, es sei denn, es wurde ein vorheriger **DocumentEvent** -Befehl mit *IESC* auf DocumentEvent \_ resetdcpre festgelegt.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DocumentEvent \_ resetdcpre**</dt> </dl>                                                                                                                                                         | GDI verarbeitet einen Aufrufen der [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) -Funktion.<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DocumentEvent \_ startdocpost**</dt> </dl>                                                                                                                                                   | GDI hat soeben einen Aufrufder [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion verarbeitet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DocumentEvent \_ startdocpre oder DocumentEvent \_ StartDoc**</dt> </dl> | GDI verarbeitet einen Aufrufen der [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion.<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DocumentEvent \_ Startpage**</dt> </dl>                                                                                                                                                            | GDI verarbeitet einen Aufrufen der [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) -Funktion.<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbin* 
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pvin* zeigt.

</dd> <dt>

*pvin* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Der Inhalt des Puffers hängt vom Wert von *IESC* ab, wie in der folgenden Tabelle gezeigt.



| Konstante                                                                                                                                                                                                                                                                                                                                               | Inhalt von pvin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DocumentEvent \_ abortdoc**</dt> </dl>                                                                                                                                                               | Nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DocumentEvent | \_ atedcpost**</dt> </dl>                                                                                                                                                   | *pvin* enthält die Adresse eines Zeigers auf die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die in einem vorherigen Aufrufen dieser Funktion im *pvout* -Parameter angegeben wurde, für den der *IESC* -Parameter auf DocumentEvent | \_ atedcpre festgelegt wurde.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DocumentEvent | \_ atedcpre**</dt> </dl>                                                                                                                                                      | *pvin* verweist auf eine DocEvent-Methode " \_ kreatedcpre", die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DocumentEvent \_ DeleteDC**</dt> </dl>                                                                                                                                                               | Nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DocumentEvent \_ enddocpost**</dt> </dl>                                                                                                                                                         | Nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DocumentEvent \_ enddocpre oder DocumentEvent \_ EndDoc**</dt> </dl>                 | Nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DocumentEvent- \_ EndPage**</dt> </dl>                                                                                                                                                                  | Nicht verwendet.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DocumentEvent-Escapezeichen \_**</dt> </dl>                                                                                                                                                                     | *pvin* verweist auf eine DocEvent- \_ Escape-Struktur, die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DocumentEvent- \_ QueryFilter**</dt> </dl>                                                                                                                                                      | Identisch mit der für DocumentEvent | \_ atedcpre.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DocumentEvent \_ resetdcpost**</dt> </dl>                                                                                                                                                      | *pvin* enthält die Adresse eines Zeigers auf die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die in einem vorherigen Aufrufen dieser Funktion im *pvout* -Parameter angegeben wurde, für den der *IESC* -Parameter auf DocumentEvent \_ resetdcpre festgelegt wurde.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DocumentEvent \_ resetdcpre**</dt> </dl>                                                                                                                                                         | *pvin* enthält die Adresse eines Zeigers auf die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die vom [**Aufrufer von ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)bereitgestellt wird.<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DocumentEvent \_ startdocpost**</dt> </dl>                                                                                                                                                   | *pvin* verweist auf einen Long-Wert, der die von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)zurückgegebene Druckauftrags-ID angibt.<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DocumentEvent \_ startdocpre oder DocumentEvent \_ StartDoc**</dt> </dl> | *pvin* enthält die Adresse eines Zeigers auf eine [**DocInfo**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) -Struktur, die vom Aufrufer von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)bereitgestellt wird.<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DocumentEvent \_ Startpage**</dt> </dl>                                                                                                                                                            | Nicht verwendet.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbout*</dt> <dd> 

| Wert                       | Bedeutung                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| idocumentevent- \_ QueryFilter | Die Größe (in Bytes) des Puffer Zeigers auf durch *pvout*.                             |
| DocumentEvent-Escapezeichen \_       | Ein Wert, der als *cboutput* -Parameter für [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)verwendet wird. |
| Für alle anderen Werte        | *IESC* wird nicht verwendet.                                                                  |



 

</dd> <dt>

*pvout* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer. Der Inhalt des Puffers hängt von dem für *IESC* angegebenen Wert ab, wie in der folgenden Tabelle dargestellt.



| Konstante                                                                                                                                                                                          | pvout-Inhalt                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DocumentEvent | \_ atedcpre**</dt> </dl> | Ein Zeiger auf eine vom Treiber angegebene [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die GDI anstelle der vom Aufrufer des [**Aufrufers angegebenen**](/windows/desktop/api/wingdi/nf-wingdi-createdca) verwendet. (Wenn **null**, verwendet GDI die vom Aufrufer angegebene Struktur.)<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DocumentEvent-Escapezeichen \_**</dt> </dl>                | Ein Zeiger auf einen Puffer, der als *lpszoutdata* -Parameter für [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)verwendet wird.<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DocumentEvent- \_ QueryFilter**</dt> </dl> | Ein Zeiger auf einen Puffer mit einer DocEvent- \_ Filter Struktur, die im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)dokumentiert ist.<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DocumentEvent \_ resetdcpre**</dt> </dl>    | Ein Zeiger auf eine vom Treiber angegebene [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die GDI anstelle der vom [**ResetDC-Aufrufer**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) angegebenen verwendet. (Wenn **null**, verwendet GDI die vom Aufrufer angegebene Struktur.)<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert der Funktion ist abhängig von der für *IESC* angegebenen Escapezeichen. Bei einigen Escapecodes wird der Rückgabewert nicht verwendet (siehe unten). Wenn die Funktion einen Rückgabewert bereitstellt, muss Sie einen der folgenden Werte aufweisen.



| Rückgabewert               | Bedeutung                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| DocumentEvent- \_ Fehler     | Der Treiber unterstützt den von *IESC* identifizierten Escapecode, aber ein Fehler ist aufgetreten. |
| DocumentEvent- \_ Erfolg     | Der Treiber hat den von *IESC* identifizierten Escapecode erfolgreich verarbeitet.             |
| DocumentEvent \_ nicht unterstützt | Der Treiber unterstützt den von *IESC* identifizierten Escapecode nicht.                 |



 

Die folgende Liste gibt an, welche Escapecodes einen Rückgabewert erfordern und welche nicht, und erläutert die Bedeutung von DocumentEvent \_ Success, DocumentEvent \_ Failure und DocumentEvent \_ nicht unterstützten Rückgabecodes.



| Rückgabewert                                          | Bedeutung                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DocumentEvent \_ abortdoc                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent | \_ atedcpost                           | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent | \_ atedcpre                            | DocumentEvent \_ -Fehler-GDI erstellt weder den Gerätekontext noch den Informations Kontext und gibt den Rückgabewert 0 für " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) " oder " [**kreateic**](/windows/desktop/api/wingdi/nf-wingdi-createica)" zurück. |
| DocumentEvent \_ DeleteDC                               | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent \_ enddocpost                             | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent \_ enddocpre oder DocumentEvent \_ EndDoc     | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent- \_ EndPage                                | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent-Escapezeichen \_                                 | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent- \_ QueryFilter                            | Siehe Hinweise.                                                                                                                                                                               |
| DocumentEvent \_ resetdcpost                            | Der Rückgabewert wird nicht verwendet und sollte nicht gelesen werden.                                                                                                                                       |
| DocumentEvent \_ resetdcpre                             | DocumentEvent \_ -Fehler-GDI setzt den Gerätekontext nicht zurück und stellt für [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)einen Rückgabewert von 0 bereit.                                                           |
| DocumentEvent \_ startdocpost                           | DocumentEvent \_ -Fehler-GDI ruft [**abortdoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) auf, um das Dokument zu verhindern, und gibt dann einen Rückgabewert des SP- \_ Fehlers für [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)an.                      |
| DocumentEvent \_ startdocpre oder DocumentEvent \_ StartDoc | DocumentEvent \_ -Fehler-GDI startet das Dokument nicht und stellt einen Rückgabewert des SP- \_ Fehlers für [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)bereit.                                                       |
| DocumentEvent \_ Startpage                              | DocumentEvent \_ -Fehler-GDI startet die Seite nicht, und gibt den Rückgabewert SP \_ Error für [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)an.                                                         |



 

## <a name="remarks"></a>Bemerkungen

Bei einem *IESC* -Wert von DocumentEvent \_ QueryFilter kann der Spooler einen \_ von **DocumentEvent** zurückgegebenen DocumentEvent-Erfolgs Wert auf zwei Arten interpretieren, je nachdem, ob der Treiber bestimmte Member der DocEvent- \_ Filter Struktur geändert hat (was im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) dokumentiert ist). (Der *pvout* -Parameter verweist auf diese-Struktur.) Wenn der Spooler Speicher für eine Struktur dieses Typs zuordnet, initialisiert er zwei Member dieser Struktur, **celementszurück gegeben** und **celementserforderlich**, zu bekannten Werten. Nachdem **DocumentEvent** zurückgegeben wurde, ermittelt der Spooler, ob sich die Werte dieser Member geändert haben, und verwendet diese Informationen, um den **DocumentEvent** -Rückgabewert zu interpretieren. Diese Situation wird in der folgenden Tabelle zusammengefasst.



| Rückgabewert                          | Status von "celementszurück gegeben" und "celementsbenötigter"    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DocumentEvent- \_ Erfolg<br/>     | Der Treiber hat an keinem Mitglied Änderungen vorgenommen.<br/> | Der Spooler interpretiert diesen Rückgabewert als äquivalent zu DocumentEvent \_ nicht unterstützt. Der Spooler kann den Ereignis Filter nicht vom Treiber abrufen, sodass er für alle Ereignisse weiterhin **DocumentEvent** aufgerufen wird.<br/>                                                                                                                                                                                                                         |
| DocumentEvent- \_ Erfolg<br/>     | Der Treiber hat eine oder beide Member geschrieben.<br/>    | Der Spooler akzeptiert diesen Rückgabewert ohne Interpretation. Wenn der Treiber nur eine von **celementsbenötigter** und **celementszurück** gibt, betrachtet der Spooler das unveränderte Element als Wert von 0 (null).<br/> Der Spooler filtert alle Ereignisse heraus, die im **adoceventcallmember** von DocEvent Filter aufgeführt sind \_ (Dies ist im [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) dokumentiert).<br/> |
| DocumentEvent \_ nicht unterstützt<br/> | Nicht verfügbar<br/>                          | Der Treiber unterstützt DocumentEvent \_ QueryFilter nicht.<br/> Der Spooler kann den Ereignis Filter nicht vom Treiber abrufen, sodass er für alle Ereignisse weiterhin **DocumentEvent** aufgerufen wird.<br/>                                                                                                                                                                                                                                            |
| DocumentEvent- \_ Fehler<br/>     | Nicht verfügbar<br/>                          | Der Treiber unterstützt DocumentEvent \_ QueryFilter, aber es ist ein interner Fehler aufgetreten.<br/> Der Spooler kann den Ereignis Filter nicht vom Treiber abrufen, sodass er für alle Ereignisse weiterhin **DocumentEvent** aufgerufen wird.<br/>                                                                                                                                                                                                                 |



 

Wenn der im *IESC* -Parameter angegebene Escapecode DocumentEvent \_ kreatedcpre ist, gelten die folgenden Regeln:

-   Wenn der Auftrag ohne Spoolvorgang direkt an den Drucker gesendet wird, verweist pvin->pszdevice auf den Drucker Namen. (Weitere Informationen finden Sie in der Dokumentation zu DocEvent \_ . Die Struktur "kreatedcpre" im [Windows-Treiberentwicklungskit](https://msdn.microsoft.com/windows/hardware/gg487428).)
-   Wenn der Auftrag gespoolgt wird, verweist pvin->pszdevice auf den Namen des Drucker Ports.

> [!Note]  
> Die folgenden Einschränkungen gelten, wenn eine 32-Bit-Anwendung auf einer 64-Bit-Version von Windows ausgeführt wird. Die einzige GDI-Funktion, die **DocumentEvent** aufruft, ist [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape), und es sollten nur private Escapezeichen verwendet werden. **DocumentEvent** -Aufrufe anderer GDI-Funktionen können zu undefiniertem Verhalten führen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Documenteventw** (Unicode) und **documenteventa** (ANSI)<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

