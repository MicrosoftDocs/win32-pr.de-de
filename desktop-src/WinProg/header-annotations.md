---
title: Header Anmerkungen
description: Header Anmerkungen beschreiben, wie eine Funktion Ihre Parameter und den Rückgabewert verwendet.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows-API, Header Datei Anmerkungen
- Header Datei Anmerkungen
- Specstrings. h
- Standard Anmerkung (Language, SAL)
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
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340281"
---
# <a name="header-annotations"></a>Header Anmerkungen

\[In diesem Thema werden die Anmerkungen beschrieben, die in den Windows-Headern durch Windows 7 unterstützt werden. Wenn Sie für Windows 8 entwickeln, sollten Sie die Anmerkungen verwenden, die in [SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120))-Anmerkungen beschrieben werden.\]

Header Anmerkungen beschreiben, wie eine Funktion Ihre Parameter und den Rückgabewert verwendet. Diese Anmerkungen wurden vielen der Windows-Header Dateien hinzugefügt, um sicherzustellen, dass Sie die Windows-API ordnungsgemäß aufrufen. Wenn Sie die Code Analyse aktivieren, die ab Visual Studio 2005 verfügbar ist, erzeugt der Compiler Warnungen der Ebene 6000, wenn Sie diese Funktionen nicht gemäß der Verwendung aufrufen, die durch die Anmerkungen beschrieben wird. Sie können diese Anmerkungen auch in Ihrem eigenen Code hinzufügen, um sicherzustellen, dass Sie ordnungsgemäß aufgerufen werden. Informationen zum Aktivieren der Code Analyse in Visual Studio finden Sie in der Dokumentation für Ihre Version von Visual Studio.

Diese Anmerkungen werden in specstrings. h definiert. Sie basieren auf primitiven, die Teil der Standard Annotation-Sprache (SAL) sind und mithilfe von implementiert werden `_declspec("SAL_*")` .

Es gibt zwei Klassen von Anmerkungen: Puffer Anmerkungen und erweiterte Anmerkungen.

## <a name="buffer-annotations"></a>Puffer Anmerkungen

Puffer Anmerkungen beschreiben, wie Funktionen ihre Zeiger verwenden, und können verwendet werden, um Pufferüberläufe zu erkennen. Jeder Parameter kann NULL oder eine Puffer Anmerkung verwenden. Eine Puffer Anmerkung wird mit einem führenden Unterstrich und den Komponenten erstellt, die in den folgenden Abschnitten beschrieben werden.



| Puffergröße                                                                                  | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*Größe*)<br/>                        | Gibt die Gesamtgröße des Puffers an. Verwenden \_ Sie mit BCOUNT und \_ ecount; verwenden Sie nicht mit \_ Part. Dieser Wert ist der barrierefreie Speicherplatz. Er ist möglicherweise kleiner als der zugewiesene Speicherplatz.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*Größe*,*Länge*)<br/> | Gibt die Gesamtgröße und die initialisierte Länge des Puffers an. Verwendung mit \_ BCOUNT \_ -Teil und \_ ecount- \_ Teil. Die Gesamtgröße ist möglicherweise kleiner als der zugewiesene Speicherplatz.<br/>              |



 



| Puffergrößen Einheiten                                                       | BESCHREIBUNG                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_BCOUNT<br/> | Die Puffergröße beträgt Byte.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | Die Puffergröße ist in-Elementen.<br/> |



 



| Richtung                                                            | BESCHREIBUNG                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_in<br/>          | Die Funktion liest aus dem Puffer. Der Aufrufer stellt den Puffer bereit und initialisiert ihn.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_INOUT<br/> | Die-Funktion liest aus und schreibt in den Puffer. Der Aufrufer stellt den Puffer bereit und initialisiert ihn. Bei Verwendung mit \_ Deref kann der Puffer von der Funktion neu zugeordnet werden.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_vorgenommen<br/>       | Die Funktion schreibt in den Puffer. Wenn die Funktion für den Rückgabewert oder mit \_ Deref verwendet wird, stellt Sie den Puffer bereit und initialisiert sie. Andernfalls stellt der Aufrufer den Puffer bereit, und die Funktion initialisiert ihn.<br/> |



 



| Dereferenzierung                                                                       | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Dereferenziert den-Parameter, um den Puffer Zeiger zu erhalten. Dieser Parameter darf nicht **null** sein.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref- \_ Opt<br/> | Dereferenziert den-Parameter, um den Puffer Zeiger zu erhalten. Dieser Parameter kann **NULL** sein.<br/>     |



 



| Initialisierung                                                    | BESCHREIBUNG                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_voll<br/> | Die Funktion initialisiert den gesamten Puffer. Nur mit Ausgabe Puffern verwenden.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_Ostteil<br/> | Mit der-Funktion wird ein Teil des Puffers initialisiert, und es wird explizit angegeben, wie viel. Nur mit Ausgabe Puffern verwenden.<br/> |



 



| Erforderlicher oder optionaler Puffer                                    | BESCHREIBUNG                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_  opt<br/> | Dieser Parameter kann **NULL** sein.<br/> |



 

Im folgenden Beispiel werden die Anmerkungen für die **GetModuleFileName** -Funktion gezeigt. Der *HMODULE* -Parameter ist ein optionaler Eingabeparameter. Der *lpFileName* -Parameter ist ein Output-Parameter. seine Größe in Zeichen wird durch den *nSize* -Parameter angegeben, und seine Länge schließt das **null**-abschließende Zeichen ein. Der *nSize* -Parameter ist ein Eingabeparameter.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Im folgenden finden Sie die Anmerkungen, die in specstrings. h definiert sind. Verwenden Sie die Informationen in den obigen Tabellen, um ihre Bedeutung zu interpretieren.

__bcount (*Größe*)  
__bcount_opt (*Größe*)  
__deref_bcount (*Größe*)  
__deref_bcount_opt (*Größe*)  
__deref_ecount (*Größe*)  
__deref_ecount_opt (*Größe*)  
__deref_in  
__deref_in_bcount (*Größe*)  
__deref_in_bcount_opt (*Größe*)  
__deref_in_ecount (*Größe*)  
__deref_in_ecount_opt (*Größe*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*Größe*)  
__deref_inout_bcount_full (*Größe*)  
__deref_inout_bcount_full_opt (*Größe*)  
__deref_inout_bcount_opt (*Größe*)  
__deref_inout_bcount_part (*Größe*,*Länge*)  
__deref_inout_bcount_part_opt (*Größe*,*Länge*)  
__deref_inout_ecount (*Größe*)  
__deref_inout_ecount_full (*Größe*)  
__deref_inout_ecount_full_opt (*Größe*)  
__deref_inout_ecount_opt (*Größe*)  
__deref_inout_ecount_part (*Größe*,*Länge*)  
__deref_inout_ecount_part_opt (*Größe*,*Länge*)  
__deref_inout_opt  
__deref_opt_bcount (*Größe*)  
__deref_opt_bcount_opt (*Größe*)  
__deref_opt_ecount (*Größe*)  
__deref_opt_ecount_opt (*Größe*)  
__deref_opt_in  
__deref_opt_in_bcount (*Größe*)  
__deref_opt_in_bcount_opt (*Größe*)  
__deref_opt_in_ecount (*Größe*)  
__deref_opt_in_ecount_opt (*Größe*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*Größe*)  
__deref_opt_inout_bcount_full (*Größe*)  
__deref_opt_inout_bcount_full_opt (*Größe*)  
__deref_opt_inout_bcount_opt (*Größe*)  
__deref_opt_inout_bcount_part (*Größe*,*Länge*)  
__deref_opt_inout_bcount_part_opt (*Größe*,*Länge*)  
__deref_opt_inout_ecount (*Größe*)  
__deref_opt_inout_ecount_full (*Größe*)  
__deref_opt_inout_ecount_full_opt (*Größe*)  
__deref_opt_inout_ecount_opt (*Größe*)  
__deref_opt_inout_ecount_part (*Größe*,*Länge*)  
__deref_opt_inout_ecount_part_opt (*Größe*,*Länge*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*Größe*)  
__deref_opt_out_bcount_full (*Größe*)  
__deref_opt_out_bcount_full_opt (*Größe*)  
__deref_opt_out_bcount_opt (*Größe*)  
__deref_opt_out_bcount_part (*Größe*,*Länge*)  
__deref_opt_out_bcount_part_opt (*Größe*,*Länge*)  
__deref_opt_out_ecount (*Größe*)  
__deref_opt_out_ecount_full (*Größe*)  
__deref_opt_out_ecount_full_opt (*Größe*)  
__deref_opt_out_ecount_opt (*Größe*)  
__deref_opt_out_ecount_part (*Größe*,*Länge*)  
__deref_opt_out_ecount_part_opt (*Größe*,*Länge*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*Größe*)  
__deref_out_bcount_full (*Größe*)  
__deref_out_bcount_full_opt (*Größe*)  
__deref_out_bcount_opt (*Größe*)  
__deref_out_bcount_part (*Größe*,*Länge*)  
__deref_out_bcount_part_opt (*Größe*,*Länge*)  
__deref_out_ecount (*Größe*)  
__deref_out_ecount_full (*Größe*)  
__deref_out_ecount_full_opt (*Größe*)  
__deref_out_ecount_opt (*Größe*)  
__deref_out_ecount_part (*Größe*,*Länge*)  
__deref_out_ecount_part_opt (*Größe*,*Länge*)  
__deref_out_opt  
__ecount (*Größe*)  
__ecount_opt (*Größe*)  
__in  
__in_bcount (*Größe*)  
__in_bcount_opt (*Größe*)  
__in_ecount (*Größe*)  
__in_ecount_opt (*Größe*)  
__in_opt  
__inout  
__inout_bcount (*Größe*)  
__inout_bcount_full (*Größe*)  
__inout_bcount_full_opt (*Größe*)  
__inout_bcount_opt (*Größe*)  
__inout_bcount_part (*Größe*,*Länge*)  
__inout_bcount_part_opt (*Größe*,*Länge*)  
__inout_ecount (*Größe*)  
__inout_ecount_full (*Größe*)  
__inout_ecount_full_opt (*Größe*)  
__inout_ecount_opt (*Größe*)  
__inout_ecount_part (*Größe*,*Länge*)  
__inout_ecount_part_opt (*Größe*,*Länge*)  
__inout_opt  
__out  
__out_bcount (*Größe*)  
__out_bcount_full (*Größe*)  
__out_bcount_full_opt (*Größe*)  
__out_bcount_opt (*Größe*)  
__out_bcount_part (*Größe*,*Länge*)  
__out_bcount_part_opt (*Größe*,*Länge*)  
__out_ecount (*Größe*)  
__out_ecount_full (*Größe*)  
__out_ecount_full_opt (*Größe*)  
__out_ecount_opt (*Größe*)  
__out_ecount_part (*Größe*,*Länge*)  
__out_ecount_part_opt (*Größe*,*Länge*)  
__out_opt  

## <a name="advanced-annotations"></a>Erweiterte Anmerkungen

Erweiterte Anmerkungen stellen zusätzliche Informationen zum Parameter oder Rückgabewert bereit. Jeder Parameter oder Rückgabewert kann NULL oder eine erweiterte Anmerkung verwenden.



| Anmerkung                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blockson (*Ressource*)<br/> | Die Functions-Blöcke für die angegebene Ressource.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_Rück<br/>                                                                        | Die-Funktion kann als Funktionszeiger verwendet werden.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_Check Return<br/>                               | Aufrufer müssen den Rückgabewert überprüfen.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_Format \_ Zeichenfolge<br/>                                                        | Der-Parameter ist eine Zeichenfolge, die den printf-Stil% Markers enthält.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount (*expr*,*size*)<br/>                            | Wenn der Ausdruck beim Beenden true ist, wird die Größe des Eingabe Puffers in Bytes angegeben. Wenn der Ausdruck false ist, wird die Größe in-Elementen angegeben.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminiert<br/>                                          | Auf den Puffer kann bis einschließlich der ersten Sequenz von zwei **null** -Zeichen oder Zeigern zugegriffen werden.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | Auf den Puffer kann bis einschließlich des ersten **null** -Zeichens oder-Zeigers zugegriffen werden.<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_Out \_ awcount (*expr*,*size*)<br/>                         | Wenn der Ausdruck beim Beenden true ist, wird die Größe des Ausgabepuffers in Bytes angegeben. Wenn der Ausdruck false ist, wird die Größe in-Elementen angegeben. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_Dire<br/>                                                                        | Gibt das c#-Stil Überschreibungs Verhalten für virtuelle Methoden an.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_bleiben<br/>                                                                        | Der-Parameter ist für die zukünftige Verwendung reserviert und muss NULL **oder NULL** sein.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_Erfolg (*expr*)<br/>                                                       | Wenn der Ausdruck beim Beenden true ist, kann der Aufrufer auf alle Garantien Vertrauen, die durch andere Anmerkungen angegeben werden. Wenn der Ausdruck false ist, kann der Aufrufer nicht auf die Garantien Vertrauen. Diese Anmerkung wird automatisch Funktionen hinzugefügt, die einen **HRESULT** -Wert zurückgeben.<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Behandeln Sie den Parameter anstelle des deklarierten Typs als den angegebenen Typ.<br/>                                                                                                                                                                                             |



 

In den folgenden Beispielen werden der Puffer und die erweiterten Anmerkungen für die Funktionen [**deletetimerqueuetimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**freumgebungs Strings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)und [**unlenker dexceptionfilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) gezeigt.


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

 

