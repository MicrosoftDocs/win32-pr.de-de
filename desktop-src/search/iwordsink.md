---
description: Behandelt Wörter, die sowohl während der Indexzeit als auch während der Abfragezeit durch Wortumbrüche identifiziert werden.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: IWordSink-Schnittstelle (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 109a852f37f3118cd1012c7385a4f9071fdd2f8867f57036e7607c20fd2dadbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822310"
---
# <a name="iwordsink-interface"></a>IWordSink-Schnittstelle

Behandelt Wörter, die sowohl während der Indexzeit als auch während der Abfragezeit durch Wortumbrüche identifiziert werden.

## <a name="members"></a>Member

Die **IWordSink-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordSink** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWordSink-Schnittstelle** verfügt über diese Methoden.



| Methode                                             | Beschreibung                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Gibt das Ende des endgültigen Ausdrucks in einer Abfolge alternativer Ausdrücke an, die eine Wörterpause während der Indexzeit generiert.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Fügt ein alternatives Wort und seine Position in das **IWordSink-Objekt** ein.<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Fügt eine Unterbrechung nach dem vorherigen Wort ein.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Fügt ein Wort und seine Position in das **IWordSink-Objekt** ein.<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Gibt die Grenze zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörterpause während der Indexzeit generiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Windows Die Suche erstellt und initialisiert Instanzen des **IWordSink-Objekts.** Das **IWordSink-Objekt** empfängt während der Initialisierung den *fQuery-Parameter* und verwendet diesen Parameter, um den Wörterbruchkontext zu bestimmen, in dem das Objekt verwendet wird.

[**IWordBreaker-Implementierungen**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) erhalten einen Zeiger auf das **IWordSink-Objekt** in der [**IWordBreaker::BreakText-Methode.**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search.h</dt> </dl> |



 

 
