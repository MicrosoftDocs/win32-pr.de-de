---
description: Beim ctrpp-Tool handelt es sich um einen Präprozessor, der das Zähler Manifest analysiert und überprüft.
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
ms.openlocfilehash: dce12de641dda7b07871a4447190772533598748
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351858"
---
# <a name="ctrpp"></a>CTRPP

Beim ctrpp-Tool handelt es sich um einen Präprozessor, der das Manifest für Ihren v2-Anbieter analysiert und überprüft. Das Tool generiert `.rc` Ressourcen mit den Zeichen folgen, die von Consumern Ihres Anbieters benötigt werden, und generiert einen `.h` Header mit Code, den Sie zum Bereitstellen der Counter-Daten verwenden. Sie sollten das ctrpp-Tool während der Erstellung Ihres Anbieters ausführen. Sie sollten den generierten Code als Ausgangspunkt verwenden, wenn Sie den Anbieter entwickeln, anstatt zu versuchen, diesen Code selbst zu generieren.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumente

|Option              |BESCHREIBUNG
|--------------------|-----------
|*Eingabedatei*         |**Erforderlich:** Gibt den Namen der `.man` (XML-Manifest)-Datei an, die ihre Leistungsindikatoren definiert.
|**-o-** *Codedatei*   |**Erforderlich:** Gibt den Namen der `.h` Codedatei an, die von ctrpp generiert werden soll. Diese Datei enthält C/C++-Inline Hilfsfunktionen, mit denen die Initialisierung und die Initialisierung des Anbieters vereinfacht werden.
|**-RC** *rcfile*    |**Erforderlich:** Gibt den Namen der `.rc` (Ressourcen Datei) an, die von ctrpp generiert werden soll. Diese Datei enthält die Zeichen folgen Tabelle des Anbieters.
|**-ch-** *symfile*   |Gibt den Namen der optionalen `.h` Symbol Datei an, die von ctrpp generiert werden soll. Diese Datei enthält C/C++-Symbole für die Namen und GUIDs der einzelnen Gegensätze im Anbieter.
|**-Präfix** *Präfix*|Gibt das Präfix an, das für die in der generierten Header Datei definierten Variablen und Funktionen verwendet werden soll.
|**-Notificationcallback**|Ändert die Standard Signatur der [**counterinitialize**](counterinitialize.md) -Funktion, um Parameter zum Angeben des Namens der Rückruf Funktionen " [*controlcallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)", " [*Zuordnungs Speicher*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)" und " [*Freispeicher*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) " einzuschließen. Dieses Argument hat denselben Effekt wie das Einschließen des- `callback` Attributs in das [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) -Element.
|**-** *OutputFile* migrieren|Anstatt `.h` -und- `.rc` Dateien zu erstellen, aktualisiert das *inputFile* -Manifest auf die neueste Version und speichert Sie in *OutputFile*. Dieser Switch kann nicht mit anderen Switches verwendet werden. Verwendung: `CTRPP -migrate NewFile.man OldFile.man`
|**-Backcompat**     |**Veraltet:** Unterstützung für Kernel Modus-Anbieter wurde in Windows 7 hinzugefügt. Standardmäßig ist der von ctrpp für kernelmodusanbieter generierte Code mit früheren Versionen von Windows nicht kompatibel (der Treiber wird aufgrund fehlender APIs nicht geladen `Pcw***` ). Legen `-BackCompat` Sie fest, um die Kompatibilität mit früheren Versionen von Windows zu aktivieren. Der Treiber lädt die erforderlichen APIs dynamisch, und der generierte Code deaktiviert den Anbieter automatisch, wenn die APIs nicht verfügbar sind.
|**-Memoryroutinen** |**Veraltet:** Bei Verwendung mit dem- `-Legacy` Schalter schließt Vorlagen für Speicher Routinen in den generierten Code ein. Andernfalls hat dieses Argument denselben Effekt wie der `-NotificationCallback` Switch.
|**-Legacy**         |**Veraltet:** Generiert `*.h` `*.c` `*.rc` die Dateien,, und `*_r.h` mithilfe der Windows Vista-Code Vorlagen (generiert perfautoinitialize und perfautocleanup anstelle von counterinitialize und countercleanup). Dieser Switch kann mit **-memoryroutinen** und **-notificationcallback** verwendet werden, kann aber nicht mit anderen Switches verwendet werden. Verwenden Sie den Schalter " **-o** " oder " **-RC** " nicht mit diesem Switch. Die generierten Dateien werden basierend auf dem Namen des Manifests benannt und in das Verzeichnis geschrieben, das das Manifest enthielt. Verwendung: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Bemerkungen

Das ctrpp-Tool generiert eine `.h` Codedatei, eine `.rc` Ressourcen Datei und generiert optional eine `.h` Symbol Datei.

### <a name="using-the-generated-resource-file"></a>Verwenden der generierten Ressourcen Datei

Das ctrpp-Tool generiert eine `.rc` Ressourcen Datei, die die lokalisierbaren Zeichen folgen enthält, die von Consumern der Anbieter-Gegensätze benötigt werden.

> [!IMPORTANT]
> Die Ressourcen aus dieser Datei müssen in der Binärdatei des Anbieters enthalten sein, und der vollständige Pfad zur Binärdatei des Anbieters muss bei der Installation des Anbieter Manifests registriert werden. Consumer, die die Ressourcen nicht finden und laden können, können die Gegensätze Ihres Anbieters nicht verwenden.

Die Zeichen folgen Ressourcen sollten wie folgt behandelt werden:

- Der Entwickler bearbeitet die Anbieter Manifest- `.man` Datei, um das- `applicationIdentity` Attribut des Anbieters auf den Namen der Binärdatei des Anbieters () festzulegen. DLL,. SYS oder. EXE), das die Zeichen folgen Ressourcen für den Anbieter enthält und als Teil der Anbieter Komponente installiert wird.
- Das ctrpp-Tool liest das Anbieter Manifest und generiert eine- `.rc` Datei.
- Mit dem RC-Tool [(Ressourcen Compiler)](../menurc/resource-compiler.md) werden die Daten aus der ctrpp-generierten `.rc` Datei kompiliert, um eine Datei zu generieren, `.res` die die binären Ressourcen enthält. Dies kann entweder durch direktes Kompilieren der ctrpp-generierten `.rc` Datei oder durch Kompilieren einer anderen `.rc` Datei erfolgen, die die durch ctrpp generierte `.rc` Datei über eine- `#include` Direktive enthält.
- Der Linker bettet die Daten aus der RC-generierten `.res` Datei in die Binärdatei des Anbieters ein.
- Während der Installation wird die Binärdatei des Anbieters auf das System des Benutzers kopiert, und das Anbieter Manifest wird mithilfe des [Lodctr-Tools](/windows-server/administration/windows-commands/lodctr)registriert. Das lodctr-Tool konvertiert das `applicationIdentity` -Attribut des Anbieter Manifests in einen vollständigen Pfad und zeichnet den vollständigen Pfad zur Binärdatei des Anbieters in der Registrierung auf.
  - Wenn sich die Anbieter Binärdatei im selben Verzeichnis wie das Manifest befindet, verwenden Sie: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr kombiniert den angegebenen manifestressfad mit dem-Attribut des Manifests `applicationIdentity` , um den vollständigen Pfad zu bilden.
  - Verwenden Sie andernfalls `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr kombiniert den angegebenen binären Pfad mit dem-Attribut des Manifests `applicationIdentity` , um den vollständigen Pfad zu bilden.
  - Zu Diagnose Zwecken können Sie den aufgezeichneten vollständigen Pfad überprüfen, indem Sie den `ApplicationIdentity` Wert des Registrierungsschlüssels überprüfen `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Wenn die Binärdatei MUI für die Lokalisierung verwendet, stellen Sie sicher, dass Sie die MUI-Datei zusammen mit der Binärdatei kopieren.
- Während der CounterSet-Auflistung verwendet der Consumer den aufgezeichneten vollständigen Pfad zur Anbieter Binärdatei, um die erforderlichen Zeichen folgen aus den Ressourcen der Anbieter Binärdatei zu suchen und zu laden.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Verwenden der generierten Codedatei in einem benutzermodusanbieter

Das ctrpp-Tool generiert eine `.h` C/C++-Codedatei. Wenn das-Attribut des Anbieter Manifests `providerType` auf festgelegt ist `userMode` , enthält die generierte Codedatei die folgenden Definitionen, die beim Programmieren eines benutzermodusanbieters hilfreich sind:

- Eine Anbieter Initialisierungsfunktion mit dem Namen [ * **prefix * counterinitialize**](counterinitialize.md).
- Eine Anbieter Bereinigungs Funktion namens [ * **prefix * countercleanup**](countercleanup.md).
- Eine Global ***Provider** _-Variable, die das von der _ *_prefix_CounterInitialize**-Funktion geöffnete Anbieter handle speichert. Der Name der Variablen ist der Wert des- `symbol` Attributs des- `provider` Elements im Manifest. Diese Variable sollte in Aufrufen von `PerfCreateInstance` , `PerfDeleteInstance` und anderen APIs zum Steuern der Daten des Anbieters verwendet werden.
- Für jede CounterSet-Variable eine Global ***CounterSet * GUID** -Variable mit der Counter Set-GUID. Der Name der Variablen ist der Wert des `counterSet` `symbol` Attributs des Elements plus des Suffixes "GUID", z. b. `MyCounterSetGUID` . Diese Variable sollte in Aufrufen von `PerfCreateInstance` , `PerfDeleteInstance` und anderen APIs zum Steuern der Daten des Anbieters verwendet werden.
- Für jeden Leistungs Bewert ein ***Counter*** -Makro mit dem Wert des Zählers `id` . Der Name des Makros ist der Wert des `counter` - `symbol` Attributs des Elements. Dieses Makro sollte in Aufrufen von `PerfSetCounterRefValue` , `PerfSetULongLongCounterValue` und anderen APIs zum Festlegen der Daten des Anbieters verwendet werden.

In den Funktionsnamen verweist ***prefix*** auf den Wert des `-prefix` Befehlszeilen Parameters. Wenn der `-prefix` -Parameter nicht verwendet wird, werden die Funktionen `CounterInitialize` und benannt `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Verwenden der generierten Codedatei in einem kernelmodusanbieter

Das ctrpp-Tool generiert eine `.h` C/C++-Codedatei. Wenn das-Attribut des Anbieter Manifests `providerType` auf festgelegt ist `kernelMode` , enthält die generierte Codedatei die folgenden Definitionen, die beim Codieren der Gegensätze eines Kernel Modus-Anbieters hilfreich sind:

- Eine CounterSet-Initialisierungsfunktion mit dem Namen " <b> *prefix* Register *counter set*</b>". Diese Funktion füllt eine [reginfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) -Struktur aus und ruft dann [pcwregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)auf, wobei das resultierende CounterSet-Registrierungs Handle in die globale ***CounterSet*** -Variable eingefügt wird.
- Eine CounterSet-Bereinigungs Funktion namens <b> *prefix* Unregister *CounterSet*</b>. Diese Funktion ruft [pcwunregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) für das CounterSet-Registrierungs Handle in der globalen ***CounterSet*** -Variable auf.
- Eine instanzerstellungs-Funktion mit dem Namen <b> *prefix* Create *CounterSet*</b>. Diese Funktion füllt ein Array von [pcwdata](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) -Strukturen auf und ruft dann [pcwkreateinstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) mit dem CounterSet-Registrierungs Handle in der globalen ***CounterSet*** -Variable auf.
- Eine instanzbereinigungs Funktion mit dem Namen <b> *prefix* close *CounterSet*</b>. Diese Funktion ruft [pcwcloseinstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance)auf.
- Eine instanzberichterstattungs-Funktion mit dem Namen <b> *prefix* fügt *CounterSet* hinzu</b> , das von der Counter Set-Rückruffunktion verwendet wird. Diese Funktion füllt ein Array von [pcwdata](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) -Strukturen aus und ruft dann [pcwaddinstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance)auf.
- **Windows SDK 20h1 und höher:** Eine reginfo-Initialisierungsfunktion mit dem Namen <b> *prefix* initregistrationinformation *CounterSet*</b> für die Verwendung in erweiterten Szenarien. Diese Funktion füllt eine [reginfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) -Struktur aus. Diese Funktion kann in Fällen verwendet werden, in denen das generierte <b> *Präfix für die Präfix* Registrierung nicht</b> Ihren Anforderungen entspricht, z. b. Wenn Sie die Werte in der reginfo-Struktur anpassen oder das zurückgegebene Handle in einer anderen Variablen speichern möchten.

In den Funktionsnamen verweist ***prefix*** auf den Wert des `-prefix` Befehlszeilen Parameters. Wenn der- `-prefix` Parameter nicht verwendet wird, haben die Funktionen kein Präfix.

> [!NOTE]
> Die generierte <b> *prefix**counter set*</b> -Funktion wird verwendet, wenn Sie über einen CounterSet-Rückruf verfügen. Die generierten <b> *Präfix* Create *CounterSet*</b> -und <b> *prefix* close *CounterSet*</b> -Funktionen werden verwendet, wenn Sie über keinen CounterSet-Rückruf verfügen.

### <a name="using-the-generated-symbol-file"></a>Verwenden der generierten Symbol Datei

Wenn der Parameter **-ch** in der Befehlszeile angegeben wird, generiert das ctrpp-Tool eine `.h` Symbol Datei. Diese Datei enthält die C/C++-Symbole für die Namen und GUIDs der einzelnen Gegensätze im Anbieter. Die Symbole können verwendet werden, wenn Programme geschrieben werden, die hart codiert sind, um die Daten aus dieser gegen Menge mit den [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md)zu nutzen.

## <a name="requirements"></a>Anforderungen

|                         ||
|-------------------------|----
| Unterstützte Mindestversion (Client)| Nur Windows Vista \[ -Desktop-Apps\]
| Unterstützte Mindestversion (Server)| Nur Windows Server 2008 \[ -Desktop-Apps\]
