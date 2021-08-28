---
title: Headeranmerkungen
description: Headeranmerkungen beschreiben, wie eine Funktion ihre Parameter und ihren Rückgabewert verwendet.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API, Headerdateianmerkungen
- Headerdateianmerkungen
- Specstrings.h
- Standardanmerkungssprache (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ad560d00c45714d0feaa9ab2fa58ff4c985730fd563d4943ff028f561f2793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643630"
---
# <a name="header-annotations"></a>Headeranmerkungen

\[In diesem Thema werden die Anmerkungen beschrieben, die in den Windows-Headern bis Windows 7 unterstützt werden. Wenn Sie für Windows 8 entwickeln, sollten Sie die anmerkungen verwenden, die unter [SAL-Anmerkungen]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120))beschrieben sind.\]

Headeranmerkungen beschreiben, wie eine Funktion ihre Parameter und ihren Rückgabewert verwendet. Diese Anmerkungen wurden vielen der Windows Headerdateien hinzugefügt, um sicherzustellen, dass Sie die Windows-API ordnungsgemäß aufrufen. Wenn Sie die Codeanalyse aktivieren, die ab dem Visual Studio 2005 verfügbar ist, erzeugt der Compiler Warnungen der Stufe 6000, wenn Sie diese Funktionen nicht gemäß der verwendungsbezogene Beschreibung durch die Anmerkungen aufrufen. Sie können diese Anmerkungen auch in Ihrem eigenen Code hinzufügen, um sicherzustellen, dass sie ordnungsgemäß aufgerufen werden. Informationen zum Aktivieren der Codeanalyse in Visual Studio finden Sie in der Dokumentation zu Ihrer Version von Visual Studio.

Diese Anmerkungen werden in Specstrings.h definiert. Sie basieren auf Primitiven, die Teil der Standardanmerkungssprache (Standard Annotation Language, SAL) sind und mit implementiert `_declspec("SAL_*")` werden.

Es gibt zwei Klassen von Anmerkungen: Pufferanmerkungen und erweiterte Anmerkungen.

## <a name="buffer-annotations"></a>Pufferanmerkungen

Pufferanmerkungen beschreiben, wie Funktionen ihre Zeiger verwenden und verwendet werden können, um Pufferüberläufe zu erkennen. Jeder Parameter kann 0 (null) oder eine Pufferanmerkung verwenden. Eine Pufferanmerkung wird mit einem führenden Unterstrich und den in den folgenden Abschnitten beschriebenen Komponenten erstellt.



| Puffergröße                                                                                  | Beschreibung                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*Size*)<br/>                        | Gibt die Gesamtgröße des Puffers an. Verwenden Sie mit \_ bcount und \_ ecount. Verwenden Sie nicht mit \_ part. Dieser Wert ist der zugängliche Bereich. er kann kleiner als der zugeordnete Speicherplatz sein.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)<br/> | Gibt die Gesamtgröße und die initialisierte Länge des Puffers an. Verwenden Sie mit \_ bcount \_ part und \_ ecount \_ part. Die Gesamtgröße kann kleiner als der zugeordnete Speicherplatz sein.<br/>              |



 



| Puffergrößeneinheiten                                                       | Beschreibung                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | Die Puffergröße ist in Bytes.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | Die Puffergröße ist in -Elementen.<br/> |



 



| Richtung                                                            | BESCHREIBUNG                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_In<br/>          | Die Funktion liest aus dem Puffer. Der Aufrufer stellt den Puffer bereit und initialisiert ihn.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_Inout<br/> | Die Funktion liest aus und schreibt in den Puffer. Der Aufrufer stellt den Puffer bereit und initialisiert ihn. Bei Verwendung mit \_ deref kann der Puffer von der Funktion neu zugeordnet werden.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_out<br/>       | Die Funktion schreibt in den Puffer. Bei Verwendung für den Rückgabewert oder mit \_ deref stellt die Funktion den Puffer bereit und initialisiert ihn. Andernfalls stellt der Aufrufer den Puffer bereit, und die Funktion initialisiert ihn.<br/> |



 



| Dereferenzierung                                                                       | Beschreibung                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Dereferenzieren Sie den Parameter, um den Pufferzeiger abzurufen. Dieser Parameter darf nicht **NULL** sein.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ opt<br/> | Dereferenzieren Sie den Parameter, um den Pufferzeiger abzurufen. Dieser Parameter kann **NULL** sein.<br/>     |



 



| Initialisierung                                                    | Beschreibung                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_Voll<br/> | Die Funktion initialisiert den gesamten Puffer. Verwenden Sie nur mit Ausgabepuffern.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_Teil<br/> | Die Funktion initialisiert einen Teil des Puffers und gibt explizit an, wie viel. Verwenden Sie nur mit Ausgabepuffern.<br/> |



 



| Erforderlicher oder optionaler Puffer                                    | Beschreibung                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span> <span id="_OPT"></span> \_opt<br/> | Dieser Parameter kann **NULL** sein.<br/> |



 

Das folgende Beispiel zeigt die Anmerkungen für die **GetModuleFileName-Funktion.** Der *hModule-Parameter* ist ein optionaler Eingabeparameter. Der *lpFilename-Parameter* ist ein Ausgabeparameter. seine Größe in Zeichen wird durch den *nSize-Parameter* angegeben, und seine Länge enthält das Zeichen mit NULL-Terminierung.  Der *nSize-Parameter* ist ein Eingabeparameter.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Im Folgenden finden Sie die Anmerkungen, die in Specstrings.h definiert sind. Verwenden Sie die Informationen in den obigen Tabellen, um ihre Bedeutung zu interpretieren.

__bcount(*Size*)  
__bcount_opt(*Size*)  
__deref_bcount(*Size*)  
__deref_bcount_opt(*Size*)  
__deref_ecount(*Size*)  
__deref_ecount_opt(*Size*)  
__deref_in  
__deref_in_bcount(*Size*)  
__deref_in_bcount_opt(*Size*)  
__deref_in_ecount(*Size*)  
__deref_in_ecount_opt(*Size*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount(*Size*)  
__deref_inout_bcount_full(*Größe*)  
__deref_inout_bcount_full_opt(*Größe*)  
__deref_inout_bcount_opt(*Größe*)  
__deref_inout_bcount_part(*size*,*length*)  
__deref_inout_bcount_part_opt(*size*,*length*)  
__deref_inout_ecount(*Größe*)  
__deref_inout_ecount_full(*Größe*)  
__deref_inout_ecount_full_opt(*Größe*)  
__deref_inout_ecount_opt(*Größe*)  
__deref_inout_ecount_part(*size*,*length*)  
__deref_inout_ecount_part_opt(*size*,*length*)  
__deref_inout_opt  
__deref_opt_bcount(*Größe*)  
__deref_opt_bcount_opt(*Größe*)  
__deref_opt_ecount(*Größe*)  
__deref_opt_ecount_opt(*Größe*)  
__deref_opt_in  
__deref_opt_in_bcount(*Größe*)  
__deref_opt_in_bcount_opt(*Größe*)  
__deref_opt_in_ecount(*Größe*)  
__deref_opt_in_ecount_opt(*Größe*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount(*Größe*)  
__deref_opt_inout_bcount_full(*Größe*)  
__deref_opt_inout_bcount_full_opt(*Größe*)  
__deref_opt_inout_bcount_opt(*Größe*)  
__deref_opt_inout_bcount_part(*size*,*length*)  
__deref_opt_inout_bcount_part_opt(*size*,*length*)  
__deref_opt_inout_ecount(*Größe*)  
__deref_opt_inout_ecount_full(*Größe*)  
__deref_opt_inout_ecount_full_opt(*Größe*)  
__deref_opt_inout_ecount_opt(*Größe*)  
__deref_opt_inout_ecount_part(*size*,*length*)  
__deref_opt_inout_ecount_part_opt(*size*,*length*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount(*Größe*)  
__deref_opt_out_bcount_full(*Größe*)  
__deref_opt_out_bcount_full_opt(*Größe*)  
__deref_opt_out_bcount_opt(*Größe*)  
__deref_opt_out_bcount_part(*size*,*length*)  
__deref_opt_out_bcount_part_opt(*size*,*length*)  
__deref_opt_out_ecount(*Größe*)  
__deref_opt_out_ecount_full(*Größe*)  
__deref_opt_out_ecount_full_opt(*Größe*)  
__deref_opt_out_ecount_opt(*Größe*)  
__deref_opt_out_ecount_part(*size*,*length*)  
__deref_opt_out_ecount_part_opt(*size*,*length*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount(*Größe*)  
__deref_out_bcount_full(*Größe*)  
__deref_out_bcount_full_opt(*Größe*)  
__deref_out_bcount_opt(*Größe*)  
__deref_out_bcount_part(*size*,*length*)  
__deref_out_bcount_part_opt(*size*,*length*)  
__deref_out_ecount(*Größe*)  
__deref_out_ecount_full(*Größe*)  
__deref_out_ecount_full_opt(*Größe*)  
__deref_out_ecount_opt(*Größe*)  
__deref_out_ecount_part(*size*,*length*)  
__deref_out_ecount_part_opt(*size*,*length*)  
__deref_out_opt  
__ecount(*Größe*)  
__ecount_opt(*Größe*)  
__in  
__in_bcount(*Größe*)  
__in_bcount_opt(*Größe*)  
__in_ecount(*Größe*)  
__in_ecount_opt(*Größe*)  
__in_opt  
__inout  
__inout_bcount(*Größe*)  
__inout_bcount_full(*Größe*)  
__inout_bcount_full_opt(*Größe*)  
__inout_bcount_opt(*Größe*)  
__inout_bcount_part(*size*,*length*)  
__inout_bcount_part_opt(*size*,*length*)  
__inout_ecount(*Größe*)  
__inout_ecount_full(*Größe*)  
__inout_ecount_full_opt(*Größe*)  
__inout_ecount_opt(*Größe*)  
__inout_ecount_part(*size*,*length*)  
__inout_ecount_part_opt(*size*,*length*)  
__inout_opt  
__out  
__out_bcount(*Größe*)  
__out_bcount_full(*Größe*)  
__out_bcount_full_opt(*Größe*)  
__out_bcount_opt(*Größe*)  
__out_bcount_part(*size*,*length*)  
__out_bcount_part_opt(*size*,*length*)  
__out_ecount(*Größe*)  
__out_ecount_full(*Größe*)  
__out_ecount_full_opt(*Größe*)  
__out_ecount_opt(*Größe*)  
__out_ecount_part(*size*,*length*)  
__out_ecount_part_opt(*size*,*length*)  
__out_opt  

## <a name="advanced-annotations"></a>Erweiterte Anmerkungen

Erweiterte Anmerkungen stellen zusätzliche Informationen zum Parameter oder Rückgabewert bereit. Jeder Parameter oder Rückgabewert kann 0 (null) oder eine erweiterte Anmerkung verwenden.



| Anmerkung                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)<br/> | Die Funktionen werden für die angegebene Ressource blockiert.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_Rückruf<br/>                                                                        | Die Funktion kann als Funktionszeiger verwendet werden.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | Aufrufer müssen den Rückgabewert überprüfen.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_\_Formatzeichenfolge<br/>                                                        | Der -Parameter ist eine Zeichenfolge, die %-Marker im Printf-Stil enthält.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount(*expr*,*size*)<br/>                            | Wenn der Ausdruck beim Beenden true ist, wird die Größe des Eingabepuffers in Bytes angegeben. Wenn der Ausdruck false ist, wird die Größe in -Elementen angegeben.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnull beendet<br/>                                          | Auf den Puffer kann bis einschließlich der ersten Sequenz von zwei **NULL-Zeichen** oder Zeigern zugegriffen werden.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_Nullterminated<br/>                                                      | Auf den Puffer kann bis einschließlich des ersten **NULL-Zeichens** oder Zeigers zugegriffen werden.<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount(*expr*,*size*)<br/>                         | Wenn der Ausdruck beim Beenden true ist, wird die Größe des Ausgabepuffers in Bytes angegeben. Wenn der Ausdruck false ist, wird die Größe in -Elementen angegeben. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_Überschreiben<br/>                                                                        | Gibt das Überschreibungsverhalten im C#-Stil für virtuelle Methoden an.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_Reserviert<br/>                                                                        | Der Parameter ist für die zukünftige Verwendung reserviert und muss 0 (null) oder **NULL** sein.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)<br/>                                                       | Wenn der Ausdruck beim Beenden true ist, kann sich der Aufrufer auf alle Garantien verlassen, die von anderen Anmerkungen angegeben werden. Wenn der Ausdruck FALSE ist, kann sich der Aufrufer nicht auf die Garantien verlassen. Diese Anmerkung wird funktionen automatisch hinzugefügt, die einen **HRESULT-Wert** zurückgeben.<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)<br/>                                                    | Behandeln Sie den Parameter als angegebenen Typ und nicht als deklarierten Typ.<br/>                                                                                                                                                                                             |



 

Die folgenden Beispiele zeigen die Puffer- und erweiterten Anmerkungen für die Funktionen [**DeleteTimerQueueTimer,**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)und [**UnhandledExceptionFilter.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SAL-Anmerkungen](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Exemplarische Vorgehensweise: Analysieren von C/C++-Code auf Fehler](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

