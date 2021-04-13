---
title: Rückgabewerte für Text Speicher (textstor. h)
description: Wenn ein Dokument-Manager einen Text Speicher verarbeitet, werden Rückgabewerte im Bereich von 0xhhhh0200 bis 0xhhhh0300 erzeugt. In der folgenden Tabelle werden die Rückgabewerte des Text Stores in alphabetischer Reihenfolge aufgelistet.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518401"
---
# <a name="text-store-return-values"></a>Rückgabewerte für Text Speicher

Wenn ein Dokument-Manager einen Text Speicher verarbeitet, werden Rückgabewerte im Bereich von 0x *HHHH* 0200 bis 0x *HHHH* 0300 erzeugt. In der folgenden Tabelle werden die Rückgabewerte des Text Stores in alphabetischer Reihenfolge aufgelistet.



| Rückgabecode/-wert                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_ E \_ Format**</dt> <dt>0x8004020a</dt> </dl>                   | Die Anwendung unterstützt nicht den Datentyp, der im [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) -Objekt enthalten ist, das mit [**ITextStoreACP:: insertemeingebettet**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)eingefügt werden soll.<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_ E \_ invalidpoint**</dt> <dt>0x80040207</dt> </dl> | Der-Parameter befindet sich nicht innerhalb des umgebenden Felds eines beliebigen Zeichens.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_ E \_ invalidpos**</dt> <dt>0x80040200</dt> </dl>       | Der angegebene Bereich erstreckt sich außerhalb des Dokuments.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>    | Das Objekt unterstützt die angeforderte Schnittstelle nicht.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_ E \_ nolayout**</dt> <dt>0x80040206</dt> </dl>             | Die Anwendung hat kein Text Layout berechnet.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                   | Die Anwendung verfügt nicht über eine schreibgeschützte Sperre oder eine Lese-/Schreibsperre für das Dokument.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>             | Der Offset für eingebettete Inhalte ist nicht vor einem TF- \_ Zeichen (Char Embedded) positioniert \_ .<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_ E \_ NoSelection**</dt> <dt>0x80040205</dt> </dl>    | Das Dokument hat keine Auswahl.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_ E \_ noservice**</dt> <dt>0x80040203</dt> </dl>          | Der Inhalt kann nicht an die Dienst-GUID zurückgegeben werden.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_ E \_**</dt> schreibgeschützt <dt>0x80040209</dt> </dl>             | Das Dokument ist schreibgeschützt. Der Inhalt kann nicht geändert werden.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_ E \_ synchrone**</dt> <dt>0x00040300</dt> </dl>    | Das Dokument kann nicht synchron gesperrt werden.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_ S \_ Async**</dt> <dt>(0x1)</dt> </dl>                         | Das Dokument hat erfolgreich eine asynchrone Sperre empfangen.<br/>                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITextStoreACP:: insertemeingebettet**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

