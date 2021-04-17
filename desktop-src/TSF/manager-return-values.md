---
title: Manager-Rückgabewerte (msctf. h)
description: Das Framework für Text Dienste erzeugt Rückgabewerte im Bereich von 0xhhhh0200 bis 0xhhhh0507. In der folgenden Tabelle werden die Werte des Vorgesetzten in alphabetischer Reihenfolge zurückgegeben.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518623"
---
# <a name="manager-return-values"></a>Manager-Rückgabewerte

Das Framework für Text Dienste erzeugt Rückgabewerte im Bereich von 0x *HHHH* 0200 bis 0x *HHHH* 0507. In der folgenden Tabelle werden die Werte des Vorgesetzten in alphabetischer Reihenfolge zurückgegeben.

> [!Note]  
> Die angegebenen Beschreibungen sind nicht spezifisch. die Bedeutung eines Rückgabewerts kann abhängig von der Methode variieren, die den Wert zurückgegeben hat.

 



| Rückgabecode/-wert                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**Tf \_ E \_ bereits \_ vorhanden**</dt> <dt>0x80040506</dt> </dl>                   | Der beibehaltene Schlüssel ist registriert.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**Tf \_ E \_ Komposition \_ abgelehnt**</dt> <dt>0x80040508</dt> </dl> | Der Kontext Besitzer hat die Komposition abgelehnt.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**Tf \_ E \_ getrennt**</dt> <dt>0x80040504</dt> </dl>                          | Das Kontext Objekt befindet sich nicht in einem Dokument Stapel.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**Tf \_ E \_ emptycontext**</dt> <dt>0x80040509</dt> </dl>                          | Der Kontext ist leer.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**Tf \_ E \_ Format**</dt> <dt>0x8004020a</dt> </dl>                                            | Der Kontext Besitzer kann die Objekte des Typs, der vom pdataobject-Parameter bereitgestellt wird, nicht verarbeiten.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**Tf \_ E \_ invalidpoint**</dt> <dt>0x80040207</dt> </dl>                          | Die Bildschirm Koordinaten sind ungültig.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**Tf \_ E \_ invalidpos**</dt> <dt>0x80040200</dt> </dl>                                | Die Zeichenposition ist ungültig.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**Tf \_ E \_ invalidview**</dt> <dt>0x80040505</dt> </dl>                             | Die Kontextansicht ist ungültig.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**Tf \_ E \_ gesperrt**</dt> <dt>0x80040500</dt> </dl>                                            | Der Kontext ist bereits gesperrt.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**Tf \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>                             | Die angeforderte Schnittstelle wird vom-Objekt nicht unterstützt.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**Tf \_ E \_ nolayout**</dt> <dt>0x80040206</dt> </dl>                                      | Das Text Layout wurde nicht berechnet.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**Tf \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                                            | Der Aufrufer verfügt nicht über den erforderlichen Dokumenttyp.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**Tf \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>                                      | An der angegebenen Position ist kein eingebettetes Objekt vorhanden.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**Tf \_ E \_ noprovider**</dt> <dt>0x80040503</dt> </dl>                                | Für die angegebene Funktion ist kein Funktions Anbieter vorhanden.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**Tf \_ E \_ NoSelection**</dt> <dt>0x80040205</dt> </dl>                             | Innerhalb des Kontexts ist keine Auswahl vorhanden.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**Tf \_ E \_ noservice**</dt> <dt>0x80040203</dt> </dl>                                   | Der angegebene Dienst ist nicht vorhanden oder kann nicht erstellt werden.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**Tf \_ E \_ notownetdrange**</dt> <dt>0x80040502</dt> </dl>                       | Der TSF-Manager besitzt den Bereich nicht.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**Tf \_ E \_ Range \_ nicht \_ abgedeckt**</dt> <dt>0x80040507</dt> </dl>         | Der Bereich befindet sich nicht innerhalb einer aktiven Komposition.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**Tf \_ E \_**</dt> schreibgeschützt <dt>0x80040209</dt> </dl>                                      | Der Bearbeitungs Kontext ist schreibgeschützt.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**Tf \_ E \_ stackfull**</dt> <dt>0x80040501</dt> </dl>                                   | Der Kontext Stapel ist voll.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**Tf \_ E \_ synchrone**</dt> <dt>0x80040208</dt> </dl>                             | Eine synchrone schreibgeschützte Sperre kann nicht abgerufen werden.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**Tf \_ S \_ Async**</dt> <dt>0x00040300</dt> </dl>                                               | Die Daten werden asynchron abgerufen.<br/>                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



 

 





