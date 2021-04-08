---
description: Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zu dem Computer Zustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt. Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden.
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
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748889"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation-Makro

Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zu dem Computer Zustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt. Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden.

> [!Note]  
> Der Microsoft C/C++-Optimierungs Compiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.

 

## <a name="syntax"></a>Syntax


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf eine [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Struktur, die Zeiger auf die folgenden zwei-Strukturen enthält:

-   [**Ausnahme \_ Daten Satz**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Struktur, die eine Beschreibung der Ausnahme enthält.
-   Die [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur, die die Computer Zustandsinformationen enthält.

## <a name="remarks"></a>Bemerkungen

Der Filter Ausdruck (von dem die Funktion aufgerufen wird) wird ausgewertet, wenn während der Ausführung des **\_ \_ try** -Blocks eine Ausnahme auftritt, und bestimmt, ob der **\_ \_ Ausnahme** Block ausgeführt wird oder nicht.

Der Filter Ausdruck kann eine Filterfunktion aufrufen. Die Filterfunktion kann **GetExceptionInformation** nicht aufrufen. Der Rückgabewert von **GetExceptionInformation** kann jedoch als Parameter an eine Filterfunktion übergeben werden.

Um die [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Informationen an den Ausnahmehandlerblock zu übergeben, muss der Filter Ausdruck oder die Filterfunktion den Zeiger oder die Daten in den sicheren Speicher kopieren, auf den der Handler später zugreifen kann.

Im Fall von schsted Handlern wird jeder Filter Ausdruck ausgewertet, bis ein Filter Ausdruck ausgewertet wird, wenn der **Ausnahme Ausführungs \_ \_ Handler** oder eine **Ausnahme \_ \_ Ausführung fortgesetzt** wird. Jeder Filter Ausdruck kann **GetExceptionInformation** aufrufen, um Ausnahme Informationen zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**Ausnahme \_ Daten Satz**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**Getxstatefeaturesmask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funktionen für die strukturierte Ausnahmebehandlung](structured-exception-handling-functions.md)
</dt> <dt>

[Übersicht über die strukturierte Ausnahmebehandlung](structured-exception-handling.md)
</dt> <dt>

[Windows-Unterstützung für Intel AVX aktivieren](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
