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
ms.openlocfilehash: eacfbb83abd56becc579c6b9bbaedacda96f94b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119105"
---
# <a name="ctrpp"></a>CTRPP

Das CTRPP-Tool ist ein Vorprozessor, der das Manifest für Ihren V2-Anbieter analysiert und überprüft. Das Tool generiert Ressourcen mit den Zeichenfolgen, die von den Kunden Ihres Anbieters benötigt werden, und generiert einen Header mit Code, mit dem Sie `.rc` `.h` Ihre Indikatordaten bereitstellen. Sie sollten das CTRPP-Tool während der Erstellung Ihres Anbieters ausführen. Sie sollten den generierten Code als Ausgangspunkt beim Entwickeln Ihres Anbieters verwenden, anstatt zu versuchen, diesen Code selbst zu generieren.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumente

|Option              |Beschreibung
|--------------------|-----------
|*inputFile*         |**Erforderlich:** Gibt den Namen der Datei `.man` (XML-Manifest) an, die Die Leistungsindikatoren definiert.
|**-o** *codeFile*   |**Erforderlich:** Gibt den Namen der Codedatei `.h` an, die von CTRPP generiert werden soll. Diese Datei enthält C/C++-Inline-Hilfsfunktionen, die die Initialisierung und Die Initialisierung Ihres Anbieters vereinfachen.
|**-rc** *rcFile*    |**Erforderlich:** Gibt den Namen der `.rc` (Ressourcendatei) an, die von CTRPP generiert werden soll. Diese Datei enthält die Zeichenfolgentabelle des Anbieters.
|**-ch** *symFile*   |Gibt den Namen der optionalen Symboldatei `.h` an, die von CTRPP generiert werden soll. Diese Datei enthält C/C++-Symbole für die Namen und GUIDs der einzelnen Countersets im Anbieter.
|**-prefix prefix** *prefix*|Gibt das Präfix an, das für die Variablen und Funktionen verwendet werden soll, die in der generierten Headerdatei definiert sind.
|**-NotificationCallback**|Ändert die Standardsignatur der [**CounterInitialize-Funktion**](counterinitialize.md) so, dass sie Parameter zum Angeben des Namens der [*Rückruffunktionen ControlCallback,*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)und [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) enthält. Dieses Argument hat die gleiche Wirkung wie das `callback` -Attribut in das [**Provider-Element.**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
|**-migrate** *outputFile*|Anstatt - und `.h` -Dateien `.rc` zu generieren, aktualisiert das *inputFile-Manifest* auf die neueste Version und speichert es in *outputFile*. Dieser Schalter kann nicht mit anderen Schaltern verwendet werden. Verwendung: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**Veraltet:** Unterstützung für Kernelmodusanbieter wurde in Windows 7 hinzugefügt. Standardmäßig ist der von CTRPP für Kernelmodusanbieter generierte Code nicht mit früheren Versionen von Windows kompatibel (der Treiber kann aufgrund fehlender `Pcw***` APIs nicht geladen werden). Legen Sie `-BackCompat` fest, um die Kompatibilität mit früheren Versionen von Windows zu aktivieren. Der Treiber wird die erforderlichen APIs dynamisch laden, und der generierte Code deaktiviert den Anbieter automatisch, wenn die APIs nicht verfügbar sind.
|**-MemoryRoutines** |**Veraltet:** Enthält bei Verwendung mit `-Legacy` dem Schalter Vorlagen für Arbeitsspeicherroutinen im generierten Code. Andernfalls hat dieses Argument die gleiche Auswirkung wie der `-NotificationCallback` Schalter.
|**-Legacy**         |**Veraltet:** Generiert -, -, - und -Dateien mithilfe der Windows Vista-Codevorlagen `*.h` `*.c` `*.rc` `*_r.h` (generiert PerfAutoInitialize und PerfAutoCleanup anstelle von CounterInitialize und CounterCleanup). Dieser Schalter kann mit **-MemoryRoutines** und **-NotificationCallback** verwendet werden, kann jedoch nicht mit anderen Switches verwendet werden. Verwenden Sie nicht die **Schalter -o** oder **-rc** mit diesem Schalter. Die generierten Dateien werden basierend auf dem Namen des Manifests benannt und in das Verzeichnis geschrieben, das das Manifest enthielt. Verwendung: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Bemerkungen

Das CTRPP-Tool generiert eine `.h` Codedatei, eine Ressourcendatei und `.rc` optional eine `.h` Symboldatei.

### <a name="using-the-generated-resource-file"></a>Verwenden der generierten Ressourcendatei

Das CTRPP-Tool generiert eine Ressourcendatei, die die lokalisierbaren Zeichenfolgen enthält, die von Denksatzverbrauchern `.rc` des Anbieters benötigt werden.

> [!IMPORTANT]
> Die Ressourcen aus dieser Datei müssen in die Binärdatei Ihres Anbieters eingeschlossen werden, und der vollständige Pfad zur Anbieterbinierung muss während der Installation des Anbietermanifests registriert werden. Benutzer, die die Ressourcen nicht finden und laden können, können die Countersets Ihres Anbieters nicht verwenden.

Die Zeichenfolgenressourcen sollten wie folgt behandelt werden:

- Der Entwickler bearbeitet die Anbietermanifestdatei ( ), um das Attribut des Anbieters auf den Namen einer Anbieterbin `.man` binären Datei (.DLL, .SYS oder .EXE) zu setzen, die die Zeichenfolgenressourcen für den Anbieter enthält und als Teil der Anbieterkomponente installiert `applicationIdentity` wird.
- Das CTRPP-Tool liest das Anbietermanifest und generiert eine `.rc` Datei.
- Das [RC-Tool (Ressourcencompiler)](../menurc/resource-compiler.md) kompiliert die Daten aus der von CTRPP generierten Datei, um eine Datei zu generieren, die `.rc` die `.res` binären Ressourcen enthält. Dies kann entweder durch direktes Kompilieren der von CTRPP generierten Datei oder durch Kompilieren einer anderen Datei erfolgen, die die von CTRPP generierte Datei über eine `.rc` `.rc` -Direktive `.rc` `#include` enthält.
- Der Linker bettet die Daten aus der rc-generierten Datei `.res` in die Anbieterbin binär ein.
- Während der Installation wird die Anbieterbinierung auf das System des Benutzers kopiert, und das Anbietermanifest wird mit dem [tool lodctr registriert.](/windows-server/administration/windows-commands/lodctr) Das tool lodctr konvertiert das Attribut des Anbietermanifests in einen vollständigen Pfad und zeichnet den vollständigen Pfad zur Anbieterbin binär `applicationIdentity` in der Registrierung auf.
  - Wenn sich die Anbieterbin binär im gleichen Verzeichnis wie das Manifest befindet, verwenden Sie : `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr kombiniert den angegebenen Manifestpfad mit dem -Attribut des Manifests, `applicationIdentity` um den vollständigen Pfad zu bilden.
  - Verwenden Sie andernfalls `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr kombiniert den angegebenen binären Pfad mit dem -Attribut des Manifests, `applicationIdentity` um den vollständigen Pfad zu bilden.
  - Zu Diagnosezwecken können Sie den aufgezeichneten vollständigen Pfad überprüfen, indem Sie den `ApplicationIdentity` Wert des Registrierungsschlüssels `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` überprüfen.
  - Wenn die Binärdatei DIE für die Lokalisierung verwendet, stellen Sie sicher, dass Sie die DATEI NRT zusammen mit der Binärdatei kopieren.
- Während der Countersetsammlung verwendet der Consumer den aufgezeichneten vollständigen Pfad zur Anbieterbinärdatei, um die erforderlichen Zeichenfolgen aus den Ressourcen der Anbieterbinärdatei zu suchen und zu laden.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Verwenden der generierten Codedatei in einem Benutzermodusanbieter

Das CTRPP-Tool generiert eine `.h` C/C++-Codedatei. Wenn das Attribut des Anbietermanifests auf festgelegt ist, enthält die generierte Codedatei die folgenden Definitionen, die beim Codieren eines `providerType` `userMode` Benutzermodusanbieters hilfreich sind:

- Eine Anbieterin initialisierungsfunktion namens [ * **prefix*CounterInitialize**](counterinitialize.md).
- Eine Anbieterbereinigungsfunktion namens [ * **prefix*CounterCleanup**](countercleanup.md).
- Eine globale ***provider** _-Variable, die das von der *__prefix_CounterInitialize *-Funktion geöffnete Anbieterhand* handle speichert. Der Name der Variablen ist der Wert des `symbol` Attributs des `provider` Elements im Manifest. Diese Variable sollte in Aufrufen von , und anderen APIs verwendet werden, um die Daten `PerfCreateInstance` `PerfDeleteInstance` Ihres Anbieters zu steuern.
- Für jedes Counterset eine globale ***Counterset*GUID-Variable** mit der Counterset-GUID. Der Name der Variablen ist der Wert des Attributs des Elements plus dem Suffix `counterSet` `symbol` "GUID", z. B. `MyCounterSetGUID` . Diese Variable sollte in Aufrufen von , und anderen APIs verwendet werden, um die Daten `PerfCreateInstance` `PerfDeleteInstance` Ihres Anbieters zu steuern.
- Für jeden Indikator ein ***Indikatormakro*** mit dem Wert des `id` Indikators. Der Name des Makros ist der Wert des `counter` Attributs des `symbol` Elements. Dieses Makro sollte in Aufrufen von , und anderen APIs zum Festlegen `PerfSetCounterRefValue` der Daten Ihres `PerfSetULongLongCounterValue` Anbieters verwendet werden.

In den Funktionsnamen ***bezieht sich prefix*** auf den Wert des `-prefix` Befehlszeilenparameters. Wenn der `-prefix` -Parameter nicht verwendet wird, werden die Funktionen und `CounterInitialize` `CounterCleanup` benannt.

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Verwenden der generierten Codedatei in einem Kernelmodusanbieter

Das CTRPP-Tool generiert eine `.h` C/C++-Codedatei. Wenn das -Attribut des Anbietermanifests auf festgelegt ist, enthält die generierte Codedatei die folgenden Definitionen, die beim Programmieren der Indikatoren eines Kernelmodusanbieters `providerType` `kernelMode` hilfreich sind:

- Eine Counterset-Initialisierungsfunktion namens <b> *Präfix* Register *Counterset*</b>. Diese Funktion füllt eine [RegInfo-Struktur](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) aus und ruft [dann PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)auf, wodurch das resultierende Counterset-Registrierungshand handle in die globale ***Counterset-Variable eingeteilt*** wird.
- Eine Counterset-Cleanupfunktion mit dem <b> *Namen präfix* Unregister *Counterset*</b>. Diese Funktion ruft [PcwUnregister für](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) das Counterset-Registrierungshand handle in der globalen ***Countersetvariablen*** auf.
- Eine Instanzerstellungsfunktion mit dem <b> *Namen präfix* Create *Counterset*</b>. Diese Funktion füllt ein Array von [PcwData-Strukturen](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) aus und ruft [dann PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) mit dem Counterset-Registrierungshandl in der globalen ***Countersetvariablen*** auf.
- Eine Instanzbereinigungsfunktion mit dem <b> *Namen präfix* Close *Counterset*</b>. Diese Funktion ruft [PcwCloseInstance auf.](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance)
- Eine Instanzberichtsfunktion mit dem Namen präfix Add Counterset to be used from the counterset callback function(Eine Instanzberichtsfunktion mit dem <b> *Namen präfix**Add Counterset,*</b> die von der Counterset-Rückruffunktion verwendet werden soll). Diese Funktion füllt ein Array von [PcwData-Strukturen](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) aus und ruft [dann PcwAddInstance auf.](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance)
- **Windows SDK 20H1 und höher:** Eine RegInfo-Initialisierungsfunktion mit <b> *dem Namen präfix* InitRegistrationInformation *Counterset zur*</b> Verwendung in erweiterten Szenarien. Diese Funktion füllt eine [RegInfo-Struktur](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) aus. Diese Funktion kann in Fällen verwendet werden, in denen das generierte Präfix <b> Register *Counterset*</b> Ihren Anforderungen nicht entspricht, z. B. wenn Sie die Werte in der RegInfo-Struktur anpassen möchten oder wenn Sie das zurückgegebene Handle in einer anderen Variablen speichern möchten.

In den Funktionsnamen ***bezieht sich prefix*** auf den Wert des `-prefix` Befehlszeilenparameters. Wenn der `-prefix` Parameter nicht verwendet wird, haben die Funktionen kein Präfix.

> [!NOTE]
> Das <b> *generierte Präfix**Counterset-Funktion*</b> hinzufügen wird verwendet, wenn Sie über einen Countersetrückruf verfügen. Die generierten <b> *Funktionen**"Counterset erstellen"*</b> und <b> *"Close Counterset"*</b> werden verwendet, wenn Sie keinen Countersetrückruf haben.

### <a name="using-the-generated-symbol-file"></a>Verwenden der generierten Symboldatei

Wenn der **Parameter -ch** in der Befehlszeile angegeben wird, generiert das CTRPP-Tool eine `.h` Symboldatei. Diese Datei enthält die C/C++-Symbole für die Namen und GUIDs jedes Countersets im Anbieter. Die Symbole können beim Schreiben von Programmen verwendet werden, die hart codiert sind, um die Daten aus diesem Counterset mithilfe der [PerfLib V2 Consumer-Funktionen](using-the-perflib-functions-to-consume-counter-data.md)zu nutzen.

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung             | Wert |
|-------------------------|-------|
| Unterstützte Mindestversion (Client)| Nur Windows \[ Vista-Desktop-Apps\]
| Unterstützte Mindestversion (Server)| Nur Windows Server \[ 2008-Desktop-Apps\]
