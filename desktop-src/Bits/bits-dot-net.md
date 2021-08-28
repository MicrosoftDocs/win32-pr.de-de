---
title: Verwenden von BITS aus .NET mitHilfe von Verweis-DLLs
description: In den folgenden Beispielen wird das Aufrufen der BITS COM-Schnittstelle aus einem .NET-Programm gezeigt.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 00f7d6287d86dd1816d7e4b0a7c6e18c9ae4916c5c85b01d0280758cf9d00b5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529150"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Aufrufen von BITS aus .NET und C# mithilfe von Verweis-DLLs

Eine Möglichkeit zum Aufrufen der BITS COM-Klassen aus einem .NET-Programm besteht in der Erstellung einer DLL-Referenzdatei, die mit den BITS [IDL-Dateien](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) im Windows SDK beginnt, indem die [MIDL-](/windows/desktop/Midl/using-the-midl-compiler-2) und [TLBIMP-Tools](/dotnet/framework/tools/tlbimp-exe-type-library-importer) verwendet werden. Die Verweis-DLL ist ein Satz von Klassen-Wrappern für die BITS COM-Klassen. Anschließend können Sie die Wrapperklassen direkt aus .NET verwenden.

Eine Alternative zur Verwendung automatisch erstellter Verweis-DLLs ist die Verwendung eines .NET BITS-Wrappers von Drittanbietern aus GitHub [und](https://github.com/) [NuGet.](https://www.nuget.org/) Diese Wrapper verfügen häufig über einen natürlicheren .NET-Programmierstil, können aber hinter den Änderungen und Updates in den BITS-Schnittstellen zurück liegen.

## <a name="creating-the-reference-dlls"></a>Erstellen der Verweis-DLLs
### <a name="bits-idl-files"></a>BITS-IDL-Dateien

Sie beginnen mit dem Satz von BITS-IDL-Dateien. Dies sind Dateien, die die BITS COM-Schnittstelle vollständig definieren. Die Dateien befinden sich im **Verzeichnis Windows Kits** und heißen bits version .idl (z.B. bits10_2.idl), mit Ausnahme der Datei version 1.0, die nur Bits.idl ist. Wenn neue Versionen von BITS erstellt werden, werden auch neue BITS-IDL-Dateien erstellt.

Sie können auch eine Kopie der SDK-BITS-IDL-Dateien ändern, um BITS-Funktionen zu verwenden, die nicht automatisch in .NET-Entsprechungen konvertiert werden. Mögliche IDL-Dateiänderungen werden später erläutert.

Die BITS-IDL-Dateien enthalten mehrere andere IDL-Dateien als Verweis. Sie schachteln sich auch, sodass sie alle niedrigeren Versionen enthalten, wenn Sie eine Version verwenden.

Für jede Version von BITS, die Sie in Ihrem Programm als Ziel verwenden möchten, benötigen Sie eine Verweis-DLL für diese Version. Wenn Sie z. B. ein Programm schreiben möchten, das auf BITS 1.5 und up funktioniert, aber über zusätzliche Features verfügt, wenn BITS 10.2 vorhanden ist, müssen Sie sowohl die dateien bits1_5.idl als auch bits10_2.idl konvertieren.


### <a name="midl-and-tlbimp-utilities"></a>MIDL- und TLBIMP-Hilfsprogramme

Das [MIDL-Hilfsprogramm](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) konvertiert die IDL-Dateien, die die BITS COM-Schnittstelle beschreiben, in eine TLB-Datei (Typbibliothek). Das MIDL-Tool ist vom CL-Hilfsprogramm (C-Präprozessor) abhängig, um die IDL-Sprachdatei ordnungsgemäß zu lesen. Das CL-Hilfsprogramm ist Teil Visual Studio und wird installiert, wenn Sie C/C++-Features in die Visual Studio.

Das MIDL-Hilfsprogramm erstellt normalerweise einen Satz von C- und H-Dateien (C-Sprachcode und C-Sprachheader). Sie können diese zusätzlichen Dateien unterdrücken, indem Sie die Ausgabe an das Gerät NUL: senden. Wenn Sie beispielsweise den Schalter /dlldata NUL: festlegen, wird das Erstellen einer dlldata.c-Datei unterdrückt. Die folgenden Beispielbefehle zeigen, welche Schalter auf NUL: festgelegt werden sollten.

Das [Hilfsprogramm TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) liest eine TLB-Datei ein und erstellt die entsprechende DLL-Referenzdatei. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Beispielbefehle für MIDL und TLBIMP

Dies ist ein Beispiel für den vollständigen Satz von Befehlen, um einen Satz von Verweisdateien zu generieren. Möglicherweise müssen Sie die Befehle basierend auf Ihrer Visual Studio- und Windows SDK-Installation und basierend auf den BITS-Features und Betriebssystemversionen ändern, auf die Sie abzielen. 

Im Beispiel wird ein Verzeichnis zum Platzieren der DLL-Referenzdateien und eine Umgebungsvariable BITSTEMP erstellt, um auf dieses Verzeichnis zu verweisen. 

Die Beispielbefehle führen dann die vsdevcmd.bat aus, die vom Installationsprogramm Visual Studio wird. Diese BAT-Datei richten Ihre Pfade und einige Umgebungsvariablen so ein, dass die MIDL- und TLBIMP-Befehle ausgeführt werden. Außerdem werden die Variablen WindowsSdkDir und WindowsSDKLibVersion so eingerichtet, dass sie auf die neuesten sdk Windows verweisen.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
Nachdem diese Befehle ausgeführt wurden, verfügen Sie über eine Reihe von Verweis-DLLs im BITSTEMP-Verzeichnis.

### <a name="adding-the-reference-dlls-to-your-project"></a>Hinzufügen der Verweis-DLLs zu Ihrem Projekt

Um eine Verweis-DLL in einem C#-Projekt zu verwenden, öffnen Sie Ihr C#-Projekt in Visual Studio. Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf die Verweise, und klicken Sie auf Verweis hinzufügen. Klicken Sie dann auf die Schaltfläche Durchsuchen und dann auf die Schaltfläche Hinzufügen. Navigieren Sie zum Verzeichnis mit den Referenz-DLLs, wählen Sie sie aus, und klicken Sie auf Hinzufügen. Im Fenster Verweis-Manager werden die Verweis-DLLs überprüft. Klicken Sie dann auf „OK“.

Die BITS-Verweis-DLLs werden ihrem Projekt jetzt hinzugefügt.

Die Informationen in den REFERENZ-DLL-Dateien werden in Ihr endgültiges Programm eingebettet. Sie müssen die DLL-Referenzdateien nicht mit Ihrem Programm versenden. Sie müssen nur die .EXE. 

Sie können ändern, ob die Verweis-DLLs in die endgültige EXE-Datei eingebettet sind. Legen Sie [mithilfe der Eigenschaft Interoptypen](/dotnet/framework/interop/how-to-add-references-to-type-libraries) einbetten fest, ob die Verweis-DLLs eingebettet werden sollen. Dies kann auf Referenzbasis erfolgen. Der Standardwert ist True zum Einbetten der DLLs.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Ändern von IDL-Dateien für vollständigeren .NET-Code

Die BITS-IDL-Dateien (Microsoft Interface Definition Language) können unverändert verwendet werden, um die BackgroundCopyManager-DLL-Datei zu erstellen. In der resultierenden .NET-Verweis-DLL fehlen jedoch einige nicht übersetzbare Unions, und sie verfügt über schwer zu verwendende Namen für einige Strukturen und Enumeren. In diesem Abschnitt werden einige der Änderungen beschrieben, die Sie vornehmen können, um die .NET-DLL vollständiger und einfacher zu verwenden.

### <a name="simpler-enum-names"></a>Einfachere ENUM-Namen

Die BITS-IDL-Dateien definieren in der Regel Aufzählwerte wie die folgenden:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
Der BG_AUTH_TARGET ist der Name der typedef. Die tatsächliche -Enum ist nicht benannt. Dies führt in der Regel nicht zu Problemen mit C-Code, lässt sich aber nicht gut für die Verwendung mit einem .NET-Programm übersetzen. Ein neuer Name wird automatisch erstellt, aber er könnte in etwa wie _MIDL___MIDL_itf_bits4_0_0005_0001_0001 statt eines für Menschen lesbaren Werts aussehen. Sie können dieses Problem beheben, indem Sie die MIDL-Dateien so aktualisieren, dass sie einen Aufenumernamen enthalten.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Der Enum-Name darf mit dem TypeDef-Namen identisch sein. Einige Programmierer haben eine Benennungskonvention, bei der sie unterschiedlich gehalten werden (z. B. durch Setzen eines Unterstrichs vor dem Namen der Aufenumer), aber dies verwirren nur die .NET-Übersetzungen. 

### <a name="string-types-in-unions"></a>Zeichenfolgentypen in Unions

Die BITS-IDL-Dateien übergeben Zeichenfolgen mithilfe der LPWSTR-Konvention (long pointer to wide-character string). Obwohl dies beim Übergeben von Funktionsparametern (z.B. der Job.GetDisplayName([out] LPWSTR *pVal)-Methode funktioniert, funktioniert dies nicht, wenn die Zeichenfolgen Teil von Unions sind. Die Datei bits5_0.idl enthält z. B. die BITS_FILE_PROPERTY_VALUE Union:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Das LPWSTR-Feld wird nicht in der .NET-Version der Union enthalten sein. Um dieses Problem zu beheben, ändern Sie LPWSTR in WCHAR*. Das resultierende Feld (string) wird als IntPtr übergeben. Konvertieren Sie dies mithilfe des Werts System.Runtime.InteropServices.Marshal.PtrToStringAuto() in eine Zeichenfolge. String); Methode.

### <a name="unions-in-structures"></a>Unions in Strukturen

Manchmal werden Unions, die in Strukturen eingebettet sind, überhaupt nicht in die Struktur aufgenommen. In der Datei Bits1_5.idl wird die BG_AUTH_CREDENTIALS wie folgt definiert:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

Die BG_AUTH_CREDENTIALS_UNION ist wie folgt als Union definiert:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Das Feld Anmeldeinformationen im BG_AUTH_CREDENTIALS nicht in der .NET-Klassendefinition enthalten.

Beachten Sie, dass die Union unabhängig vom BG_BASIC_CREDENTIALS immer als BG_AUTH_SCHEME. Da die Union nicht als Union verwendet wird, können wir einfach wie BG_BASIC_CREDENTIALS übergeben:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Verwenden von BITS aus C #

### <a name="recommended-using-statement"></a>Empfohlene Using-Anweisung

Durch das Einrichten einiger using-Anweisungen in C# wird die Anzahl der Zeichen reduziert, die Sie eingeben müssen, um die verschiedenen BITS-Versionen zu verwenden. Der Name "BITSReference" stammt aus dem Namen der Verweis-DLL.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Schnellbeispiel: Herunterladen einer Datei

Unten finden Sie einen kurzen, aber vollständigen Codeausschnitt mit C#-Code zum Herunterladen einer Datei von einer URL. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

In diesem Beispielcode wird ein BITS-Manager namens mgr erstellt. Er entspricht direkt der [IBackgroundCopyManager-Schnittstelle.](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) 

Vom Vorgesetzten wird ein neuer Auftrag erstellt. Der Auftrag ist ein out-Parameter für die CreateJob-Methode. Ebenfalls übergeben wird der Auftragsname (der nicht eindeutig sein muss) und der Downloadtyp, bei dem es sich um einen Downloadauftrag handelt. Eine BITS-GUID für den Auftragsbezeichner wird ebenfalls ausgefüllt.

Nachdem der Auftrag erstellt wurde, fügen Sie dem Auftrag mit der AddFile-Methode eine neue Downloaddatei hinzu. Sie müssen zwei Zeichenfolgen übergeben: eine für die Remotedatei (die URL oder Dateifreigabe) und eine für die lokale Datei. 

Nachdem Sie die Datei hinzugefügt haben, rufen Sie Resume für den Auftrag auf, um sie zu starten. Anschließend wartet der Code, bis sich der Auftrag in einem endgültigen Zustand (ERROR oder TRANSFERD) befindet, und wird dann abgeschlossen.

### <a name="bits-versions-casting-and-queryinterface"></a>BITS-Versionen, Umwandlung und QueryInterface

Sie werden feststellen, dass Sie häufig sowohl eine frühe Version eines BITS-Objekts als auch eine neuere Version in Ihrem Programm verwenden müssen.  

Wenn Sie beispielsweise ein Auftragsobjekt erstellen, erhalten Sie einen IBackgroundCopyJob (Teil der BITS-Version 1.0), auch wenn Sie es mit einem neueren Managerobjekt erstellen und ein neueres IBackgroundCopyJob-Objekt verfügbar ist. Da die CreateJob-Methode keine Schnittstelle für die neuere Version akzeptiert, können Sie die neuere Version nicht direkt erstellen.

Verwenden Sie eine .NET-Umwandlung, um von einem älteren Typobjekt in ein neueres Typobjekt zu konvertieren. Die Cast-Zeichenfolge wird automatisch ein COM QueryInterface aufrufen. 

In diesem Beispiel gibt es ein BITS IBackgroundCopyJob-Objekt namens "job", und wir möchten es in ein IBackgroundCopyJob5-Objekt namens "job5" konvertieren, damit wir die BITS 5.0 GetProperty-Methode aufrufen können. Wir haben einfach in den IBackgroundCopyJob5-Typ wie den folgenden umstellen:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

Die Job5-Variable wird von .NET mit der richtigen QueryInterface initialisiert. 

Wenn Ihr Code möglicherweise auf einem System ausgeführt wird, das keine bestimmte Version von BITS unterstützt, können Sie die Cast-Ausnahme ausprobieren und die System.InvalidCastException abfangen. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Ein häufiges Problem ist, wenn Sie versuchen, in die falsche Art von Objekt zu casten. Das .NET-System weiß nicht über die tatsächliche Beziehung zwischen den BITS-Schnittstellen. Wenn Sie nach der falschen Art von Schnittstelle fragen, versucht .NET, sie für Sie zu erstellen, und es wird ein Fehler mit einer InvalidCastException und einer HResult-0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Arbeiten mit BITS-Versionen 10_1 und 10_2

In einigen Versionen von Windows 10 können Sie ein BITS IBackgroundCopyManager-Objekt nicht direkt mithilfe der Schnittstellen 10.1 oder 10.2 erstellen. Stattdessen müssen Sie mehrere Versionen der BackgroundCopyManager-DLL-Verweisdateien verwenden. Beispielsweise können Sie die Version 1.5 verwenden, um ein IBackgroundCopyManager-Objekt zu erstellen, und dann die resultierenden Auftrags- oder Dateiobjekte mithilfe der Versionen 10.1 oder 10.2 casten.

