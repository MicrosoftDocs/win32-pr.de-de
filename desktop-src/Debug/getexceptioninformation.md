---
description: Ruft eine computerunabhängige Beschreibung einer Ausnahme sowie Informationen zum Computerzustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt. Diese Funktion kann nur innerhalb des Filterausdrucks eines Ausnahmehandlers aufgerufen werden.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation-Makro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 425cfbe10ac2ee66f10e016489ff070b67b6fc243a472f95b4f5809724998a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279220"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation-Makro

Ruft eine computerunabhängige Beschreibung einer Ausnahme sowie Informationen zum Computerzustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt. Diese Funktion kann nur innerhalb des Filterausdrucks eines Ausnahmehandlers aufgerufen werden.

> [!Note]  
> Der Microsoft C/C++-Optimierungscompiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Ausnahmebehandlungssyntax generiert einen Compilerfehler.

 

## <a name="syntax"></a>Syntax


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf eine [**EXCEPTION \_ POINTERS-Struktur,**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) die Zeiger auf die folgenden beiden -Strukturen enthält:

-   [**EXCEPTION \_ RECORD-Struktur,**](/windows/desktop/api/WinNT/ns-winnt-exception_record) die eine Beschreibung der Ausnahme enthält.
-   [**CONTEXT-Struktur,**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) die die Computerzustandsinformationen enthält.

## <a name="remarks"></a>Hinweise

Der Filterausdruck (aus dem die Funktion aufgerufen wird) wird ausgewertet, wenn während der Ausführung des **\_ \_ try-Blocks** eine Ausnahme auftritt, und bestimmt, ob der **\_ \_ ausnahme-Block** ausgeführt wird.

Der Filterausdruck kann eine Filterfunktion aufrufen. Die Filterfunktion kann **GetExceptionInformation** nicht aufrufen. Der Rückgabewert von **GetExceptionInformation** kann jedoch als Parameter an eine Filterfunktion übergeben werden.

Um die [**EXCEPTION \_ POINTERS-Informationen**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) an den Ausnahmehandlerblock zu übergeben, muss der Filterausdruck oder die Filterfunktion den Zeiger oder die Daten in einen sicheren Speicher kopieren, auf den der Handler später zugreifen kann.

Bei geschachtelten Handlern wird jeder Filterausdruck ausgewertet, bis einer als **EXCEPTION \_ EXECUTE \_ HANDLER** oder **EXCEPTION CONTINUE \_ \_ EXECUTION** ausgewertet wird. Jeder Filterausdruck kann **GetExceptionInformation** aufrufen, um Ausnahmeinformationen abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**\_AUSNAHMEZEIGER**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**EXCEPTION \_ RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Strukturierte Funktionen zur Ausnahmebehandlung](structured-exception-handling-functions.md)
</dt> <dt>

[Übersicht über die strukturierte Ausnahmebehandlung](structured-exception-handling.md)
</dt> <dt>

[Aktivieren der Windows-Unterstützung für Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
