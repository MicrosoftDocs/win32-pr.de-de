---
title: Verwenden von Bits aus .NET mithilfe von Verweis-DLLs
description: In den folgenden Beispielen wird gezeigt, wie die Bits-com-Schnittstelle aus einem .NET-Programm aufgerufen wird.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719583"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Aufrufen von Bits aus .net und c# mithilfe von Verweis-DLLs

Eine Möglichkeit, die Bits-com-Klassen aus einem .NET-Programm aufzurufen, besteht darin, eine Verweis-dll-Datei zu erstellen, die mit den Bits [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language)-Dateien im Windows SDK beginnt, mithilfe der Tools " [Mittel l](/windows/desktop/Midl/using-the-midl-compiler-2) " und " [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) " Die Verweis-dll ist ein Satz von Klassen-Wrappern für die Bits-com-Klassen. Anschließend können Sie die Wrapper Klassen direkt aus .NET verwenden.

Eine Alternative zur Verwendung automatisch erstellter Verweis-DLLs ist die Verwendung eines .net-Bits-Wrappers von Drittanbietern von [GitHub](https://github.com/) und [nuget](https://www.nuget.org/). Diese Wrapper verfügen häufig über einen natürlicheren .net-Programmierstil, Sie können jedoch hinter den Änderungen und Aktualisierungen in den Bits-Schnittstellen liegen.

## <a name="creating-the-reference-dlls"></a>Erstellen der Verweis-DLLs
### <a name="bits-idl-files"></a>Bits-IDL-Dateien

Sie beginnen mit dem Satz von Bits-IDL-Dateien. Dies sind Dateien, die die Bits-com-Schnittstelle vollständig definieren. Die Dateien befinden sich im Verzeichnis " **Windows Kits** " und heißen Bits-*Version*. idl (z. b. bits10_2. idl), mit Ausnahme der Datei der Version 1,0, die nur Bits. idl ist. Wenn neue Versionen von Bits erstellt werden, werden auch neue Bits-IDL-Dateien erstellt.

Möglicherweise möchten Sie auch eine Kopie der SDK Bits-IDL-Dateien ändern, um Bits-Funktionen zu verwenden, die nicht automatisch in .NET-Entsprechungen konvertiert werden. Mögliche Änderungen an der IDL-Datei werden später erläutert.

Die Bits-IDL-Dateien enthalten mehrere andere IDL-Dateien als Verweis. Sie schachteln auch, sodass Sie bei Verwendung einer Version alle niedrigeren Versionen enthält.

Für jede Version von Bits, die in Ihrem Programm als Ziel verwendet werden soll, benötigen Sie eine Verweis-dll für diese Version. Wenn Sie z. b. ein Programm schreiben möchten, das mit Bits 1,5 und up funktioniert, aber zusätzliche Funktionen aufweist, wenn Bits 10,2 vorhanden ist, müssen Sie sowohl die bits1_5. idl-als auch die bits10_2. IDL-Dateien konvertieren.


### <a name="midl-and-tlbimp-utilities"></a>Mittel l-und Tlbimp-Hilfsprogramme

Das Hilfsprogramm " [Mittel l](/windows/desktop/Midl/using-the-midl-compiler-2) " (Microsoft Interface Definition Language) konvertiert die IDL-Dateien, die die Bits-com-Schnittstelle beschreiben, in eine TLB-Datei (Typbibliothek). Das Tool "Mittel l" hängt vom CL-Hilfsprogramm (C-Präprozessor) ab, um die IDL-Sprachdatei ordnungsgemäß zu lesen. Das CL-Hilfsprogramm ist Teil von Visual Studio und wird installiert, wenn Sie C/C++-Funktionen in die Visual Studio-Installation einbinden.

Das Hilfsprogramm "Mittelwert" erstellt normalerweise einen Satz von c-und H-Dateien (c-Sprachcode und c-sprach Header). Sie können diese zusätzlichen Dateien unterdrücken, indem Sie die Ausgabe an das NUL:-Gerät senden. Wenn Sie z. b. den/dlldata NUL: Switch festlegen, wird das Erstellen einer dlldata. c-Datei unterdrückt. Die folgenden Beispiel Befehle zeigen, welche Switches auf NUL festgelegt werden sollten:.

Das Hilfsprogramm [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Typbibliotheks Import) liest in eine TLB-Datei und erstellt die entsprechende Verweis-dll-Datei. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Beispiel Befehle für "Mittel l" und "Tlbimp"

Dies ist ein Beispiel für den kompletten Satz von Befehlen, um einen Satz von Verweis Dateien zu generieren. Möglicherweise müssen Sie die Befehle auf der Grundlage Ihrer Visual Studio-und Windows SDK Installation ändern und auf der Grundlage der Bits-Features und Betriebssystemversionen, auf die Sie abzielen. 

Im Beispiel wird ein Verzeichnis erstellt, in dem die dll-Referenzdateien abgelegt werden, und es wird eine Umgebungsvariable bitwort p erstellt, um auf dieses Verzeichnis zu verweisen 

Mit den Beispiel Befehlen führen Sie dann die vsdevcmd.bat Datei aus, die vom Visual Studio-Installer erstellt wurde. Mit dieser bat-Datei werden Ihre Pfade und einige Umgebungsvariablen so eingerichtet, dass die Befehle "Mittel l" und "Tlbimp" ausgeführt werden. Außerdem werden die Variablen WindowsSdkDir und windowssdklibversion so eingerichtet, dass Sie auf die neuesten Windows SDK Verzeichnisse zeigen.

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
Nachdem diese Befehle ausgeführt wurden, verfügen Sie über eine Reihe von Verweis-DLLs im Verzeichnis "bitstemp".

### <a name="adding-the-reference-dlls-to-your-project"></a>Hinzufügen der Verweis-DLLs zu Ihrem Projekt

Öffnen Sie das c#-Projekt in Visual Studio, um eine Verweis-dll in einem c#-Projekt zu verwenden. Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf Verweise, und klicken Sie dann auf Verweis hinzufügen. Klicken Sie dann auf die Schaltfläche zum Durchsuchen und dann auf die Schaltfläche Navigieren Sie zu dem Verzeichnis mit den Verweis-DLLs, wählen Sie Sie aus, und klicken Sie auf hinzufügen. Im Fenster "Verweis-Manager" werden die Verweis-DLLs geprüft. Klicken Sie dann auf „OK“.

Die Bits-Verweis-DLLs werden nun dem Projekt hinzugefügt.

Die Informationen in den Verweis-dll-Dateien werden in das endgültige Programm eingebettet. Sie müssen die dll-Referenzdateien nicht an Ihr Programm senden. Sie müssen lediglich das versenden. Speichert. 

Sie können ändern, ob die Verweis-DLLs in die endgültige exe-Datei eingebettet werden. Verwenden Sie die Eigenschaft [Interop-Typen einbetten](/dotnet/framework/interop/how-to-add-references-to-type-libraries) , um festzulegen, ob die Verweis-DLLs eingebettet werden. Dies kann auf Verweis Basis erfolgen. Der Standardwert ist "true", um die DLLs einzubetten.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Ändern von IDL-Dateien für einen ausführlicheren .NET-Code

Die Bits-IDL-Dateien (Microsoft Interface Definition Language) können unverändert verwendet werden, um die backgroundcopymanager-dll-Datei zu erstellen. Allerdings fehlen in der resultierenden .net-Verweis-dll einige nicht übersetzbare Unions und verfügt über schwer zu verwendende Namen für einige Strukturen und enums. In diesem Abschnitt werden einige der Änderungen beschrieben, die Sie vornehmen können, um die .net-dll zu vervollständigen und leichter zu verwenden.

### <a name="simpler-enum-names"></a>Einfachere Enum-Namen

Die Bits-IDL-Dateien definieren in der Regel Enumerationswerte wie folgt:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
Der BG_AUTH_TARGET ist der Name der typedef. die tatsächliche Aufzählung wird nicht benannt. Dies verursacht in der Regel keine Probleme mit C-Code, lässt sich jedoch nicht gut für die Verwendung mit einem .NET-Programm umsetzen. Ein neuer Name wird automatisch erstellt, kann aber in etwa wie _MIDL___MIDL_itf_bits4_0_0005_0001_0001 aussehen, anstelle eines lesbaren Werts. Sie können dieses Problem beheben, indem Sie die mittleren Dateien so aktualisieren, dass Sie einen Enumeration-Namen enthalten.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Der Enumeration-Name darf nicht mit dem Typedef-Namen identisch sein. Einige Programmierer verfügen über eine Benennungs Konvention, bei der Sie anders gehalten werden (z. b. durch Einfügen eines Unterstrichs vor dem Enumeration-Namen), aber dies verwechselt nur die .net-Übersetzungen. 

### <a name="string-types-in-unions"></a>Zeichen folgen Typen in Unions

Die Bits-IDL-Dateien übergeben Zeichen folgen mithilfe der LPWSTR-Konvention (Long-Zeiger auf breit Zeichen Zeichenfolge). Dies funktioniert zwar beim Übergeben von Funktionsparametern (wie z. b. die Job. getDisplayName ([out] LPWSTR * PVal)-Methode), aber es funktioniert nicht, wenn die Zeichen folgen zu Unions gehören. Die bits5_0. IDL-Datei enthält z. b. die BITS_FILE_PROPERTY_VALUE Union:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Das Feld "LPWSTR" ist nicht in der .NET-Version der Union enthalten. Um dieses Problem zu beheben, ändern Sie "LPWSTR" in "WCHAR *". Das resultierende Feld (so genannte Zeichenfolge) wird als IntPtr übergeben. Konvertieren Sie diese in eine Zeichenfolge mithilfe von System. Runtime. InteropServices. Marshal. ptrumstringauto (Value). Zeichenfolge); anzuwenden.

### <a name="unions-in-structures"></a>Unions in Strukturen

Manchmal sind Unions, die in Strukturen eingebettet sind, nicht in der Struktur enthalten. Beispielsweise wird in der Bits1_5. idl die BG_AUTH_CREDENTIALS wie folgt definiert:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

Der BG_AUTH_CREDENTIALS_UNION wird wie folgt als Union definiert:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Das Feld Anmelde Informationen im BG_AUTH_CREDENTIALS wird nicht in die .net-Klassendefinition eingeschlossen.

Beachten Sie, dass die Union so definiert ist, dass Sie unabhängig von der BG_AUTH_SCHEME immer ein BG_BASIC_CREDENTIALS ist. Da die Union nicht als Union verwendet wird, können wir einfach eine BG_BASIC_CREDENTIALS wie die folgende übergeben:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Verwenden von Bits aus C #

### <a name="recommended-using-statement"></a>Empfohlene using-Anweisung

Wenn Sie einige using-Anweisungen in c# einrichten, verringern Sie die Anzahl der Zeichen, die Sie eingeben müssen, um die verschiedenen Bits-Versionen zu verwenden. Der Name "bizreference" stammt aus dem Namen der Verweis-dll.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Kurzes Beispiel: Herunterladen einer Datei

Im folgenden finden Sie einen kurzen, aber kompletten Ausschnitt von c#-Code zum Herunterladen einer Datei aus einer URL. 

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

In diesem Beispielcode wird ein Bits-Manager mit dem Namen "Mgr" erstellt. Sie entspricht direkt der [ibackgroundcopymanager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) -Schnittstelle. 

Aus dem Manager wird ein neuer Auftrag erstellt. Der Auftrag ist ein out-Parameter in der Methode "kreatejob". Außerdem wird der Name des Auftrags (der nicht eindeutig sein muss) und der Downloadtyp, bei dem es sich um einen Download Auftrag handelt, übermittelt. Außerdem wird eine Bits-GUID für den Auftrags Bezeichner ausgefüllt.

Nachdem der Auftrag erstellt wurde, fügen Sie dem Auftrag mit der AddFile-Methode eine neue Downloaddatei hinzu. Sie müssen zwei Zeichen folgen übergeben, eine für die Remote Datei (URL oder Dateifreigabe) und eine für die lokale Datei. 

Nachdem Sie die Datei hinzugefügt haben, können Sie den Auftrag fortsetzen, um ihn zu starten. Dann wartet der Code, bis sich der Auftrag in einem abschließenden Zustand befindet (Fehler oder übertragen) und dann abgeschlossen wird.

### <a name="bits-versions-casting-and-queryinterface"></a>Bits-Versionen, Umwandlung und QueryInterface

Sie werden feststellen, dass Sie häufig sowohl eine frühe Version eines Bits-Objekts als auch eine neuere Version in Ihrem Programm verwenden müssen.  

Wenn Sie z. b. ein Auftrags Objekt erstellen, erhalten Sie einen ibackgroundcopyjob (Teil der Bits-Version 1,0), auch wenn Sie ihn mit einem neueren Manager-Objekt erstellen und ein aktuelleres ibackgroundcopyjob-Objekt verfügbar ist. Da die Methode "kreatejob" eine Schnittstelle für die aktuellste Version nicht akzeptiert, können Sie die aktuellste Version nicht direkt erstellen.

Verwenden Sie eine .net-Umwandlung, um von einem älteren Typobjekt in ein neueres Typobjekt zu konvertieren. Die Umwandlung ruft automatisch eine COM-QueryInterface-Schnittstelle auf. 

In diesem Beispiel gibt es ein ibackgroundcopyjob-Objekt mit dem Namen "Job", und wir möchten es in ein IBackgroundCopyJob5-Objekt mit dem Namen "job5" konvertieren, damit wir die Methode "Bits 5,0 GetProperty" aufrufen können. Wir haben einfach wie folgt eine Umwandlung in den IBackgroundCopyJob5-Typ durch:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

Die job5-Variable wird von .NET mithilfe der korrekten QueryInterface initialisiert. 

Wenn Ihr Code möglicherweise auf einem System ausgeführt wird, das eine bestimmte Version von Bits nicht unterstützt, können Sie die Umwandlung ausprobieren und die System. InvalidCastException-Ausnahme abfangen. 

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

Ein häufiges Problem ist, wenn Sie versuchen, eine Umwandlung in die falsche Art von Objekt durchführen. Das .NET-System kennt die wirkliche Beziehung zwischen den Bits-Schnittstellen nicht. Wenn Sie nach der falschen Art der Schnittstelle gefragt werden, versucht .net, Sie für Sie zu verwenden, und es tritt ein Fehler mit InvalidCastException und HRESULT 0x80004002 (E_NOINTERFACE) auf.

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Arbeiten mit Bits-Versionen 10_1 und 10_2

In einigen Versionen von Windows 10 können Sie kein Bits-ibackgroundcopymanager-Objekt direkt mithilfe der 10,1-oder 10,2-Schnittstellen erstellen. Stattdessen müssen Sie mehrere Versionen der Referenzdateien der backgroundcopymanager-dll verwenden. Beispielsweise können Sie die Version 1,5 verwenden, um ein ibackgroundcopymanager-Objekt zu erstellen, und dann die resultierenden Aufträge oder Datei Objekte mithilfe der Versionen 10,1 oder 10,2 umwandeln.

