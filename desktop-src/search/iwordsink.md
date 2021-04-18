---
description: Behandelt Wörter, die von Wort Umbrüchen während der Index Zeit und der Abfragezeit identifiziert werden.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Iwordsink-Schnittstelle (Search. h)
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
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344672"
---
# <a name="iwordsink-interface"></a>Iwordsink-Schnittstelle

Behandelt Wörter, die von Wort Umbrüchen während der Index Zeit und der Abfragezeit identifiziert werden.

## <a name="members"></a>Member

Die **iwordsink** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwordsink** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwordsink** -Schnittstelle verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Endaltphrase**](iwordsink-endaltphrase.md)     | Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.<br/>  |
| [**Putaltword**](iwordsink-putaltword.md)         | Fügt ein alternatives Wort und seine Position in das **iwordsink** -Objekt ein.<br/>                                                       |
| [**Putbreak**](iwordsink-putbreak.md)             | Versetzt nach dem vorangehenden Wort einen Umbruch.<br/>                                                                                       |
| [**Putword**](iwordsink-putword.md)               | Fügt ein Wort und seine Position in das **iwordsink** -Objekt ein.<br/>                                                                    |
| [**Startaltphrase**](iwordsink-startaltphrase.md) | Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Windows Search erstellt und Initialisiert Instanzen des **iwordsink** -Objekts. Das **iwordsink** -Objekt empfängt den *fquery* -Parameter während der Initialisierung und verwendet diesen Parameter, um den Wort Umbruch Kontext zu bestimmen, in dem das-Objekt verwendet wird.

[**Iwordbreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) -Implementierungen erhalten einen Zeiger auf das **iwordsink** -Objekt in der [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search. h</dt> </dl> |



 

 
