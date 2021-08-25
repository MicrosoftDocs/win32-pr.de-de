---
description: Das CTRPP-Tool ist ein Vorprozessor, der Ihr Indikatormanifest analysiert und überprüft.
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8c55e9f3b95d99feabac92574a4be59dacb8ffd7f3b55be07c2bd8fec576da86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033930"
---
# <a name="ctrpp"></a>CTRPP

Das CTRPP-Tool ist ein Vorprozessor, der das Manifest für Ihren V2-Anbieter analysiert und überprüft. Das Tool generiert `.rc` Ressourcen mit den Zeichenfolgen, die von Consumern Ihres Anbieters benötigt werden, und generiert einen `.h` Header mit Code, den Sie zum Bereitstellen Ihrer Indikatordaten verwenden. Sie sollten das CTRPP-Tool während der Erstellung Ihres Anbieters ausführen. Sie sollten den generierten Code als Ausgangspunkt für die Entwicklung Ihres Anbieters verwenden, anstatt selbst zu versuchen, diesen Code zu generieren.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumente

|Option              |BESCHREIBUNG
|--------------------|-----------
|*inputFile*         |**Erforderlich:** Gibt den Namen der `.man` (XML-Manifest)-Datei an, die Ihre Leistungsindikatoren definiert.
|**-o** *codeFile*   |**Erforderlich:** Gibt den Namen der `.h` Codedatei an, die von CTRPP generiert werden soll. Diese Datei enthält C/C++-Inlinehilfsfunktionen, die das Initialisieren und Aufheben der Initialisierung Ihres Anbieters vereinfachen.
|**-rc** *rcFile*    |**Erforderlich:** Gibt den Namen der `.rc` (Ressourcendatei) an, die von CTRPP generiert werden soll. Diese Datei enthält die Zeichenfolgentabelle des Anbieters.
|**-ch** *symFile*   |Gibt den Namen der optionalen `.h` Symboldatei an, die von CTRPP generiert werden soll. Diese Datei enthält C/C++-Symbole für die Namen und GUIDs jedes Countersets im Anbieter.
|**-prefix** *prefix*|Gibt das Präfix an, das für die Variablen und Funktionen verwendet werden soll, die in der generierten Headerdatei definiert sind.
|**-NotificationCallback**|Ändert die Standardsignatur der [**CounterInitialize-Funktion,**](counterinitialize.md) um Parameter zum Angeben des Namens der [*Rückruffunktionen ControlCallback,*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)und [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) einzuschließt. Dieses Argument hat die gleiche Auswirkung wie das Einschließen des `callback` -Attributs in das [**Provider-Element.**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
|**-migrate** *outputFile*|Anstatt `.h` - und `.rc` -Dateien zu generieren, aktualisiert das *inputFile-Manifest* auf die neueste Version und speichert es in *outputFile.* Dieser Schalter kann nicht mit anderen Schaltern verwendet werden. Syntax: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**Veraltet:** Unterstützung für Kernelmodusanbieter wurde in Windows 7 hinzugefügt. Standardmäßig ist der von CTRPP für Kernelmodusanbieter generierte Code nicht mit früheren Versionen von Windows kompatibel (der Treiber kann aufgrund fehlender APIs nicht geladen `Pcw***` werden). Legen Sie diese Einstellung `-BackCompat` fest, um die Kompatibilität mit früheren Versionen von Windows zu aktivieren. Der Treiber lädt die erforderlichen APIs dynamisch, und der generierte Code deaktiviert den Anbieter automatisch, wenn die APIs nicht verfügbar sind.
|**-MemoryRoutines** |**Veraltet:** Enthält bei Verwendung mit dem `-Legacy` Schalter Vorlagen für Speicherroutinen im generierten Code. Andernfalls hat dieses Argument die gleiche Auswirkung wie der `-NotificationCallback` Schalter.
|**-Legacy**         |**Veraltet:** Generiert `*.h` dateien , , und `*.c` `*.rc` `*_r.h` mithilfe der Windows Vista-Codevorlagen (generiert PerfAutoInitialize und PerfAutoCleanup anstelle von CounterInitialize und CounterCleanup). Dieser Schalter kann mit **-MemoryRoutines** und **-NotificationCallback** verwendet werden, aber nicht mit anderen Schaltern. Verwenden Sie nicht die Schalter **-o** oder **-rc** mit diesem Switch. Die generierten Dateien werden basierend auf dem Namen des Manifests benannt und in das Verzeichnis geschrieben, das das Manifest enthielt. Syntax: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Hinweise

Das CTRPP-Tool generiert eine `.h` Codedatei, eine `.rc` Ressourcendatei und optional eine `.h` Symboldatei.

### <a name="using-the-generated-resource-file"></a>Verwenden der generierten Ressourcendatei

Das CTRPP-Tool generiert eine `.rc` Ressourcendatei, die die lokalisierbaren Zeichenfolgen enthält, die von Consumern der Countersets des Anbieters benötigt werden.

> [!IMPORTANT]
> Die Ressourcen aus dieser Datei müssen in der Anbieterbinärdatei enthalten sein, und der vollständige Pfad zur Anbieterbinärdatei muss während der Installation des Anbietermanifests registriert werden. Consumer, die die Ressourcen nicht finden und laden können, können die Countersets Ihres Anbieters nicht verwenden.

Die Zeichenfolgenressourcen sollten wie folgt behandelt werden:

- Der Entwickler bearbeitet die `.man` Anbietermanifestdatei (), um das `applicationIdentity` Attribut des Anbieters auf den Namen einer Anbieterbinärdatei (.DLL, .SYS oder .EXE) festzulegen, die die Zeichenfolgenressourcen für den Anbieter enthält und als Teil der Anbieterkomponente installiert wird.
- Das CTRPP-Tool liest das Anbietermanifest und generiert eine `.rc` Datei.
- Das [RC-Tool (Ressourcencompiler)](../menurc/resource-compiler.md) kompiliert die Daten aus der von CTRPP generierten `.rc` Datei, um eine Datei mit den binären Ressourcen zu `.res` generieren. Dies kann entweder durch direktes Kompilieren der CTRPP-generierten `.rc` Datei oder durch Kompilieren einer anderen `.rc` Datei erfolgen, die die von CTRPP generierte `.rc` Datei über eine `#include` -Direktive enthält.
- Der Linker bettet die Daten aus der RC-generierten `.res` Datei in die Anbieterbinärdatei ein.
- Während der Installation wird die Anbieterbinärdatei auf das System des Benutzers kopiert, und das Anbietermanifest wird mit dem [lodctr-Tool](/windows-server/administration/windows-commands/lodctr)registriert. Das lodctr-Tool konvertiert das `applicationIdentity` Attribut des Anbietermanifests in einen vollständigen Pfad und zeichnet den vollständigen Pfad zur Anbieterbinärdatei in der Registrierung auf.
  - Wenn sich die Anbieterbinärdatei im selben Verzeichnis wie das Manifest befindet, verwenden Sie `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` : . lodctr kombiniert den angegebenen Manifestpfad mit dem -Attribut des `applicationIdentity` Manifests, um den vollständigen Pfad zu bilden.
  - Verwenden Sie andernfalls `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr kombiniert den angegebenen binären Pfad mit dem -Attribut des `applicationIdentity` Manifests, um den vollständigen Pfad zu bilden.
  - Zu Diagnosezwecken können Sie den aufgezeichneten vollständigen Pfad überprüfen, indem Sie den `ApplicationIdentity` Wert des Registrierungsschlüssels `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` überprüfen.
  - Wenn die Binärdatei FÜR die Lokalisierung VERWENDET, stellen Sie sicher, dass Sie die DATEIENDR-Datei zusammen mit der Binärdatei kopieren.
- Während der Countersetsammlung verwendet der Consumer den aufgezeichneten vollständigen Pfad zur Anbieterbinärdatei, um die erforderlichen Zeichenfolgen aus den Ressourcen der Anbieterbinärdatei zu suchen und zu laden.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Verwenden der generierten Codedatei in einem Benutzermodusanbieter

Das CTRPP-Tool generiert eine `.h` C/C++-Codedatei. Wenn das Attribut des Anbietermanifests `providerType` auf festgelegt `userMode` ist, enthält die generierte Codedatei die folgenden Definitionen, die beim Codieren eines Benutzermodusanbieters hilfreich sind:

- Eine Anbieterinitialisierungsfunktion namens [ * **prefix*CounterInitialize**](counterinitialize.md).
- Eine Anbieterbereinigungsfunktion namens [ * **prefix*CounterCleanup**](countercleanup.md).
- Eine globale ***Anbietervariable**, die das von der *__prefix_CounterInitialize**-Funktion geöffnete Anbieterhandle speichert. Der Name der Variablen ist der Wert des `symbol` Attributs des `provider` Elements im Manifest. Diese Variable sollte in Aufrufen von `PerfCreateInstance` `PerfDeleteInstance` , und anderen APIs zum Steuern der Daten Ihres Anbieters verwendet werden.
- Für jedes Counterset eine globale ***Counterset*GUID-Variable** mit der Counterset-GUID. Der Name der Variablen ist der Wert des Attributs des `counterSet` Elements plus dem Suffix `symbol` "GUID", z. B. `MyCounterSetGUID` . Diese Variable sollte in Aufrufen von `PerfCreateInstance` `PerfDeleteInstance` , und anderen APIs zum Steuern der Daten Ihres Anbieters verwendet werden.
- Für jeden Indikator ein ***Indikatormakro*** mit dem Wert des Zählers. `id` Der Name des Makros ist der Wert des `counter` Attributs des `symbol` Elements. Dieses Makro sollte in Aufrufen von `PerfSetCounterRefValue` `PerfSetULongLongCounterValue` , und anderen APIs zum Festlegen der Daten Ihres Anbieters verwendet werden.

In den Funktionsnamen bezieht sich ***prefix*** auf den Wert des `-prefix` Befehlszeilenparameters. Wenn der `-prefix` Parameter nicht verwendet wird, werden die Funktionen `CounterInitialize` und `CounterCleanup` benannt.

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Verwenden der generierten Codedatei in einem Kernelmodusanbieter

Das CTRPP-Tool generiert eine `.h` C/C++-Codedatei. Wenn das Attribut des Anbietermanifests `providerType` auf festgelegt `kernelMode` ist, enthält die generierte Codedatei die folgenden Definitionen, die beim Codieren der Countersets eines Kernelmodusanbieters hilfreich sind:

- Eine Countersetinitialisierungsfunktion namens <b> *präfix* Register *Counterset*</b>. Diese Funktion füllt eine [RegInfo-Struktur](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) aus und ruft dann [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)auf und legt das resultierende Counterset-Registrierungshandle in die globale ***Counterset-Variable*** ein.
- Eine Countersetbereinigungsfunktion mit dem Namen <b> *präfix* Unregister *Counterset*</b>. Diese Funktion ruft [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) für das Countersetregistrierungshandle in der globalen ***Counterset-Variablen*** auf.
- Eine Instanzerstellungsfunktion mit dem Namen <b> *präfix**Counterset* erstellen.</b> Diese Funktion füllt ein Array von [PcwData-Strukturen](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) aus und ruft dann [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) mithilfe des Counterset-Registrierungshandle in der globalen ***Counterset-Variablen*** auf.
- Eine Instanzbereinigungsfunktion namens <b> *präfix* Close *Counterset*</b>. Diese Funktion ruft [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance)auf.
- Eine Instanzberichterstellungsfunktion mit dem Namen <b> *präfix**Add Counterset,*</b> die von der Countersetrückruffunktion verwendet werden soll. Diese Funktion füllt ein Array von [PcwData-Strukturen](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) aus und ruft dann [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance)auf.
- **Windows SDK 20H1 und höher:** Eine RegInfo-Initialisierungsfunktion mit dem Namen <b> *präfix* InitRegistrationInformation *Counterset*</b> zur Verwendung in erweiterten Szenarien. Diese Funktion füllt eine [RegInfo-Struktur](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) aus. Diese Funktion kann in Fällen verwendet werden, in denen das generierte <b> *Präfix* Register *Counterset*</b> Ihre Anforderungen nicht erfüllt, z. B. wenn Sie die Werte in der RegInfo-Struktur anpassen möchten oder wenn Sie das zurückgegebene Handle in einer anderen Variablen speichern möchten.

In den Funktionsnamen bezieht sich ***prefix*** auf den Wert des `-prefix` Befehlszeilenparameters. Wenn der `-prefix` Parameter nicht verwendet wird, haben die Funktionen kein Präfix.

> [!NOTE]
> Die generierte <b> *Präfixfunktion**Counterset* hinzufügen</b> wird verwendet, wenn Sie über einen Countersetrückruf verfügen. Die generierten <b> *Funktionen**"Counterset erstellen"*</b> und <b> *"Close Counterset"*</b> werden verwendet, wenn Sie keinen Countersetrückruf haben.

### <a name="using-the-generated-symbol-file"></a>Verwenden der generierten Symboldatei

Wenn der **-ch-Parameter** in der Befehlszeile angegeben wird, generiert das CTRPP-Tool eine `.h` Symboldatei. Diese Datei enthält die C/C++-Symbole für die Namen und GUIDs jedes Countersets im Anbieter. Die Symbole können beim Schreiben von Programmen verwendet werden, die hart codiert sind, um die Daten aus diesem Counterset mithilfe der [PerfLib V2 Consumer-Funktionen](using-the-perflib-functions-to-consume-counter-data.md)zu nutzen.

## <a name="requirements"></a>Anforderungen

| Anforderung             | Wert |
|-------------------------|-------|
| Unterstützte Mindestversion (Client)| Windows \[Nur Vista-Desktop-Apps\]
| Unterstützte Mindestversion (Server)| Windows Nur Server \[ 2008-Desktop-Apps\]
