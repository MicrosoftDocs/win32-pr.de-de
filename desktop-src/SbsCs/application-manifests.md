---
description: Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Anwendungsmanifeste
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: a1ced7ffb4052f418e989e907f26abb85c2c63db
ms.sourcegitcommit: 25211012b002a7d1303e438277373d7faf958a68
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122436708"
---
# <a name="application-manifests"></a>Anwendungsmanifeste

Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll. Dabei sollte es sich um die gleichen Assemblyversionen handeln, die zum Testen der Anwendung verwendet wurden. Anwendungsmanifeste können auch Metadaten für private Anwendungsdateien beschreiben.

Eine vollständige Liste des XML-Schemas finden Sie unter [Manifestdateischema](manifest-file-schema.md).

Anwendungsmanifesten verfügen über die folgenden Elemente und Attribute.

| Element                               | Attribute                | Erforderlich |
|---------------------------------------|---------------------------|----------|
| **Versammlung**                          |                           | Ja      |
|                                       | **manifestVersion**       | Ja      |
| **noInherit**                         |                           | Nein       |
| **Assemblyidentity**                  |                           | Ja      |
|                                       | **type**                  | Ja      |
|                                       | **name**                  | Ja      |
|                                       | **language**              | Nein       |
|                                       | **processorArchitecture** | Nein       |
|                                       | **version**               | Ja      |
|                                       | **Publickeytoken**        | Nein       |
| **Kompatibilität**                     |                           | Nein       |
| **application**                       |                           | Nein       |
| **supportedOS**                       | **Id**                    | Nein       |
| **maxversiontested**                  | **Id**                    | Nein       |
| **Abhängigkeit**                        |                           | Nein       |
| **Dependentassembly**                 |                           | Nein       |
| **datei**                              |                           | Nein       |
|                                       | **name**                  | Nein       |
|                                       | **Hashalg**               | Nein       |
|                                       | **hash**                  | Nein       |
| **activeCodePage**                    |                           | Nein       |
| **autoElevate**                       |                           | Nein       |
| **disableTheming**                    |                           | Nein       |
| **disableWindowFiltering**            |                           | Nein       |
| **dpiAware**                          |                           | Nein       |
| **dpiAwareness**                      |                           | Nein       |
| **gdiScaling**                        |                           | Nein       |
| **highResolutionScrollingAware**      |                           | Nein       |
| **longPathAware**                     |                           | Nein       |
| **printerDriverIsolation**            |                           | Nein       |
| **ultraHighResolutionScrollingAware** |                           | Nein       |
| **msix**                              |                           | Nein       |
| **heapType**                          |                           | Nein       |

## <a name="file-location"></a>Speicherort

Anwendungsmanifeste sollten als Ressource in der EXE-Datei oder DLL der Anwendung enthalten sein.

Weitere Informationen finden Sie unter [Installieren von nebenseitigen Assemblys.](installing-side-by-side-assemblies.md)

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name einer Anwendungsmanifestdatei ist der Name der ausführbaren Datei der Anwendung gefolgt von .manifest.

Beispielsweise würde ein Anwendungsmanifest, das auf example.exe oder example.dll, die folgende Dateinamensyntax verwenden. Sie können die Ressourcen-ID <*Felds>,* wenn die Ressourcen-ID 1 ist.

***example.exe.<-Ressourcen-ID*>.manifest**

***example.dll.<-Ressourcen-ID*>.manifest**

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme des Werts des Typattributs.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>Assembly

Ein Containerelement. Das erste Unterelement muss ein **noInherit- oder** **assemblyIdentity-Element** sein. Erforderlich.

Das **Assemblyelement** muss sich im Namespace "urn:schemas-microsoft-com:asm.v1" befinden. Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.

Das **Assemblyelement** verfügt über die folgenden Attribute.



| Attribut           | Beschreibung                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | Das **manifestVersion-Attribut** muss auf 1.0 festgelegt werden. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Schließen Sie dieses Element in ein Anwendungsmanifest ein, um die [aktivierungskontexte,](activation-contexts.md) die aus dem Manifest generiert werden, mit dem Flag "No inherit" festzulegen. Wenn dieses Flag nicht in einem Aktivierungskontext festgelegt ist und der Aktivierungskontext aktiv ist, wird es von neuen Threads im gleichen Prozess, fenster, fensterprozeduren und [asynchronen Prozeduraufrufen](/windows/desktop/Sync/asynchronous-procedure-calls)geerbt. Durch Festlegen dieses Flags wird verhindert, dass das neue Objekt den aktiven Kontext erbt.

Das **noInherit-Element** ist optional und wird in der Regel ausgelassen. Die meisten Assemblys funktionieren nicht ordnungsgemäß mithilfe eines Aktivierungskontexts ohne Erben, da die Assembly explizit entworfen werden muss, um die Weitergabe ihres eigenen Aktivierungskontexts zu verwalten. Die Verwendung des **noInherit-Elements** erfordert, dass alle abhängigen Assemblys, auf die vom Anwendungsmanifest verwiesen wird, über ein **noInherit-Element** im [Assemblymanifest verfügen.](assembly-manifests.md)

Wenn **noInherit** in einem Manifest verwendet wird, muss es das erste Unterelement des **Assemblyelements** sein. Das **assemblyIdentity-Element** sollte unmittelbar nach dem **noInherit-Element** vorhanden sein. Wenn **noInherit** nicht verwendet wird, muss **assemblyIdentity** das erste Unterelement des **Assemblyelements** sein. Das **noInherit-Element** verfügt über keine untergeordneten Elemente. Es ist kein gültiges Element in [Assemblymanifesten.](assembly-manifests.md)

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Als erstes Unterelement eines **Assemblyelements** beschreibt **assemblyIdentity** die Anwendung, die dieses Anwendungsmanifest besitzt, und identifiziert sie eindeutig. **AssemblyIdentity** beschreibt als erstes Unterelement eines **dependentAssembly-Elements** eine für die Anwendung erforderliche nebenseitige Assembly. Beachten Sie, dass jede Assembly, auf die im Anwendungsmanifest verwiesen wird, eine **assemblyIdentity** erfordert, die genau der **assemblyIdentity** im eigenen Assemblymanifest der Assembly entspricht, auf die verwiesen wird.

Das **assemblyIdentity-Element** verfügt über die folgenden Attribute. Sie verfügt über keine Unterelemente.

| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Gibt den Anwendungs- oder Assemblytyp an. Der Wert muss Win32 und alle in Kleinbuchstaben sein. Erforderlich.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Gibt der Anwendung oder Assembly einen eindeutigen Namen. Verwenden Sie das folgende Format für den Namen: Organization.Division.Name. Beispiel: Microsoft. Windows.mysampleApp. Erforderlich.                                                                                                                                                                                                                                                               |
| **language**              | Gibt die Sprache der Anwendung oder Assembly an. Optional. Wenn die Anwendung oder Assembly sprachspezifisch ist, geben Sie den DHTML-Sprachcode an. In der **assemblyIdentity** einer Anwendung, die für die weltweite Verwendung vorgesehen ist (sprachneutral), wird das Sprachattribut weggelassen.<br/> Legen Sie in einer **assemblyIdentity** einer Assembly für die weltweite Verwendung (sprachneutral) den Wert der Sprache auf \* fest.<br/> |
| **processorArchitecture** | Gibt den Prozessor an. Gültige Werte sind `x86`, `amd64`, `arm` und `arm64`. Optional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Gibt die Anwendungs- oder Assemblyversion an. Verwenden Sie das vierteilige Versionsformat: mmmmm.nnnnn.ooooo.apkpp. Jeder teil, der durch Zeiträume getrennt ist, kann 0-65535 einschließlich sein. Weitere Informationen finden Sie unter [Assemblyversionen.](assembly-versions.md) Erforderlich.                                                                                                                                                                        |
| **Publickeytoken**        | Eine Hexadezimalzeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Anwendung oder Assembly signiert ist. Der zum Signieren des Katalogs verwendete öffentliche Schlüssel muss 2.048 Bit oder höher sein. Erforderlich für alle freigegebenen nebeneinander verwendeten Assemblys.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>Kompatibilität

Enthält mindestens eine **Anwendung.** Sie verfügt über keine Attribute. Optional. Anwendungsmanifeste ohne Kompatibilitätselement Windows vista-Kompatibilität standardmäßig auf Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Enthält mindestens ein **supportedOS-Element.** Ab Windows 10 Version 1903 kann es auch ein optionales **maxversiontested-Element** enthalten. Sie verfügt über keine Attribute. Optional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

Das **supportedOS-Element** weist das folgende Attribut auf. Sie verfügt über keine Unterelemente.

| Attribut | Beschreibung   |
|-----------|-----------------------|
| **Id**    | Legen Sie das Id-Attribut auf **{e2011457-1546-43c5-a5fe-008deee3d3f0}** fest, um die Anwendung mit vista-Funktionalität auszuführen. Dadurch kann eine Anwendung, die für Windows Vista entwickelt wurde, unter einem späteren Betriebssystem ausgeführt werden. <br/> Legen Sie das Id-Attribut auf **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** fest, um die Anwendung mit Windows 7-Funktionalität auszuführen.<br/> Anwendungen, die Windows Vista-, Windows 7- und Windows 8-Funktionalität unterstützen, erfordern keine separaten Manifeste. Fügen Sie in diesem Fall die GUIDs für alle Windows Betriebssysteme hinzu.<br/> Informationen zum Verhalten des **ID-Attributs** in Windows finden Sie im [Windows 8 und Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Die folgenden GUIDs entsprechen den angegebenen Betriebssystemen:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 und Windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 und Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 und Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 und Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista und Windows Server 2008<br/> Sie können dies auf Windows 7 oder Windows 8.x testen, indem Sie Ressourcenmonitor (Resmon) ausführen, zur Registerkarte CPU gelangen, mit der rechten Maustaste auf die Spaltenbezeichnungen "Spalte auswählen..." klicken und "Betriebssystemkontext" aktivieren. Auf Windows 8.x finden Sie diese Spalte auch im Task-Manager (taskmgr). Der Inhalt der Spalte zeigt den höchsten gefundenen Wert oder "Windows Vista" als Standardwert an. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

Das **maxversiontested-Element** gibt die Versionen von Windows an, für die die Anwendung getestet wurde, beginnend mit der minimalen Betriebssystemversion, die die Anwendung bis zur maximalen Version unterstützt. Den vollständigen Satz von Versionen finden Sie [hier.](https://developer.microsoft.com/windows/downloads/sdk-archive/) Dies ist für Desktopanwendungen vorgesehen, die [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) verwenden und nicht in einem MSIX-Paket bereitgestellt werden. Dieses Element wird in Windows 10 Version 1903 und höher unterstützt.

Das **maxversiontested-Element** weist das folgende Attribut auf. Sie verfügt über keine Unterelemente.

| Attribut | Beschreibung    |
|-----------|----------------|
| **Id**    | Legen Sie das Id-Attribut auf eine vierteilige Versionszeichenfolge fest, die die maximale Version von Windows angibt, mit der die Anwendung getestet wurde. Beispiel: "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Enthält mindestens eine **dependentAssembly-**. Sie verfügt über keine Attribute. Optional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Das erste Unterelement von **dependentAssembly** muss ein **assemblyIdentity-Element** sein, das eine für die Anwendung erforderliche side-by-side-Assembly beschreibt. Jede **dependentAssembly** muss sich innerhalb genau einer **Abhängigkeit** befinden. Sie verfügt über keine Attribute.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

Gibt Dateien an, die für die Anwendung privat sind. Optional.

Das **Dateielement** verfügt über die In der folgenden Tabelle gezeigten Attribute.



| Attribut   | Beschreibung                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Der Name der Datei. Beispiel: Comctl32.dll.                                                            |
| **Hashalg** | Algorithmus, der zum Erstellen eines Hashs der Datei verwendet wird. Dieser Wert sollte SHA1 sein.                                 |
| **hash**    | Ein Hash der Datei, auf die anhand des Namens verwiesen wird. Eine hexadezimale Zeichenfolge der Länge, die vom Hashalgorithmus abhängt. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Auf Windows 10 erzwingt dieses Element, dass ein Prozess UTF-8 als Prozesscodepage verwendet. Weitere Informationen finden Sie unter [Verwenden der UTF-8-Codepage.](/windows/uwp/design/globalizing/use-utf8-code-page) Auf Windows 10 ist **UTF-8** der einzige gültige Wert für **activeCodePage.**

Ab Windows 11 ermöglicht dieses Element auch die Auswahl der Legacy-Codepage, die nicht UTF-8 ist, oder der Codepages für ein bestimmtes Gebietsschema, um die Kompatibilität der Legacyanwendung zu gewährleisten. Modernen Anwendungen wird dringend empfohlen, Unicode zu verwenden. Auf Windows 11 kann **activeCodePage** auch auf den Wert **Legacy** oder einen Gebietsschemanamen wie **en-US** oder **ja-JP** festgelegt werden.

- Auf Computern, die für eine aktive UTF-8-Systemcodepage konfiguriert sind, wird der Prozess von **Legacy** auf die Codepages des Systemschemas zurückgesetzt. Wenn das Systemschema keine definierten Codepages enthält, wird Windows-1252/437 verwendet. Die Einstellung **Legacycodepage** wird nur in Fusion-Manifesten und erst ab Windows 11 unterstützt.
- Wenn ein Gebietsschemaname wie **en-US** angegeben wird, wird die Prozesscodepage entsprechend für diese Gebietsschema-Codepage festgelegt. Beispiel: Windows-1252 und 437 für en-US oder 932 für ja-JP.

Dieses Element wurde erstmals in Windows 10 Version 1903 (Update vom Mai 2019) hinzugefügt. Sie können diese Eigenschaft deklarieren und auf früheren Windows Builds als Ziel bzw. ausführen, aber Sie müssen die Erkennung und Konvertierung von Legacycodeseiten wie gewohnt behandeln. Dieses Element weist keine Attribute auf. 

Im folgenden Beispiel wird veranschaulicht, wie sie dieses Element verwenden, um zu erzwingen, dass der aktuelle Prozess UTF-8 als Prozesscodepage verwendet.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>autoElevate

Gibt an, ob die automatische Erhöhung von Rechten aktiviert ist. **TRUE** gibt an, dass sie aktiviert ist. Sie verfügt über keine Attribute.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Gibt an, ob das Angeben von Benutzeroberflächenelementen in einem Design deaktiviert ist. **TRUE** gibt an, dass deaktiviert ist. Sie verfügt über keine Attribute.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Gibt an, ob die Fensterfilterung deaktiviert werden soll. **TRUE** deaktiviert die Fensterfilterung, sodass Sie immersive Fenster über den Desktop aufzählen können. **disableWindowFiltering** wurde in Windows 8 hinzugefügt und weist keine Attribute auf.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>dpiAware

Gibt an, ob der aktuelle Prozess Punkt pro Zoll (DPI) erkennt.

**Windows 10 Version 1607:** Das **dpiAware-Element** wird ignoriert, wenn das **dpiAwareness-Element** vorhanden ist. Sie können beide Elemente in ein Manifest einschließen, wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten.

In der folgenden Tabelle wird das Verhalten beschrieben, das sich basierend auf dem Vorhandensein des **dpiAware-Elements** und des darin enthaltenen Texts ergibt. Beim Text innerhalb des Elements wird die Groß-/Kleinschreibung nicht beachtet.

| Status des **dpiAware-Elements** | Beschreibung     |
|-----------------------------------|---------|
| „Absent“                            | Der aktuelle Prozess ist standardmäßig nicht dpi. Sie können diese Einstellung programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.                                                                                                                                                            |
| Enthält "true"                   | Der aktuelle Prozess ist systemdpi-fähigen.                                                                                                                                                                                                                                                                                                                                                          |
| Enthält "false"                  | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist nicht dpi-basiert, und Sie können diese Einstellung nicht programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.<br/> |
| Enthält "true/pm"                | **Windows Vista, Windows 7 und Windows 8:** Der aktuelle Prozess ist systemdpi-fähigen.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.<br/>                                                                                                                                                                                                          |
| Enthält "pro Monitor"            | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.<br/>                                                                                                                                                                                      |
| Enthält eine beliebige andere Zeichenfolge.         | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist nicht dpi-basiert, und Sie können diese Einstellung nicht programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.<br/> |

Weitere Informationen zu DPI-Einstellungen finden Sie unter [Vergleich der DPI-Wahrnehmungsstufen.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

**dpiAware** weist keine Attribute auf.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>dpiAwareness

Gibt an, ob der aktuelle Prozess Punkt pro Zoll (DPI) erkennt.

Die Mindestversion des Betriebssystems, das das **dpiAwareness-Element** unterstützt, ist Windows 10 Version 1607. Bei Versionen, die das **dpiAwareness-Element** unterstützen, überschreibt **dpiAwareness** das **dpiAware-Element.** Sie können beide Elemente in ein Manifest einschließen, wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten.

Das **dpiAwareness-Element** kann ein einzelnes Element oder eine Liste von durch Trennzeichen getrennten Elementen enthalten. Im letzteren Fall wird das erste (ganz links) Element in der Liste verwendet, das vom Betriebssystem erkannt wird. Auf diese Weise können Sie unterschiedliche Verhaltensweisen angeben, die in zukünftigen Windows Betriebssystemversionen unterstützt werden.

In der folgenden Tabelle wird das Verhalten beschrieben, das sich ergibt, basierend auf dem Vorhandensein des **dpiAwareness-Elements** und des Texts, der in seinem am weitesten links erkannten Element enthalten ist. Beim Text innerhalb des Elements wird die Groß-/Kleinschreibung nicht beachtet.

| **dpiAwareness-Elementstatus:**        | Beschreibung                          |
|-----------------------------------------|-------------------------------------------|
| Das Element ist nicht vorhanden.                       | Das **dpiAware-Element** gibt an, ob der Prozess dpi-fähigen Ist.                                                                                                                                                                   |
| Enthält keine erkannten Elemente            | Der aktuelle Prozess ist standardmäßig nicht dpi. Sie können diese Einstellung programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen. |
| Das erste erkannte Element ist "system".       | Der aktuelle Prozess ist systemdpi-fähigen.                                                                                                                                                                                               |
| Das erste erkannte Element ist "permonitor".   | Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.                                                                                                                                                                                          |
| Das erste erkannte Element ist "permonitorv2". | Im aktuellen Prozess wird der DPI-Kontext pro Monitor-v2 verwendet. Dieses Element wird nur in Windows 10 Version 1703 oder höher erkannt.                                                                                              |
| Das erste erkannte Element ist "nicht bekannt".      | Der aktuelle Prozess ist dpi nicht bekannt. Sie können diese Einstellung **nicht** programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.      |

Weitere Informationen zu DPI-Einstellungen, die von diesem Element unterstützt werden, finden Sie unter [DPI \_ AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) und [DPI \_ AWARENESS \_ CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).

**dpiAwareness** weist keine Attribute auf.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

Gibt an, ob die GDI-Skalierung aktiviert ist. Die Mindestversion des Betriebssystems, das das **gdiScaling-Element** unterstützt, ist Windows 10 Version 1703.

Das GDI-Framework (Grafikgeräteschnittstelle) kann die DPI-Skalierung auf Primitive und Text pro Monitor anwenden, ohne die Anwendung selbst zu aktualisieren. Dies kann nützlich sein, wenn GDI-Anwendungen nicht mehr aktiv aktualisiert werden.

Nichtvektorgrafiken (z. B. Bitmaps, Symbole oder Symbolleisten) können von diesem Element nicht skaliert werden. Darüber hinaus können Grafiken und Text, die in Bitmaps angezeigt werden, die dynamisch von Anwendungen erstellt werden, auch nicht von diesem Element skaliert werden.

**TRUE** gibt an, dass dieses Element aktiviert ist. Sie verfügt über keine Attribute.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

Gibt an, ob bildlauffähiges Bildlauf mit hoher Auflösung aktiviert ist. **TRUE** gibt an, dass sie aktiviert ist. Sie verfügt über keine Attribute.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Aktiviert lange Pfade, die **MAX_PATH** überschreiten. Dieses Element wird in Windows 10 Version 1607 und höher unterstützt. Weitere Informationen finden Sie in [diesem Artikel](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

Gibt an, ob die Druckertreiberisolation aktiviert ist. **TRUE** gibt an, dass sie aktiviert ist. Sie verfügt über keine Attribute. Die Druckertreiberisolation verbessert die Zuverlässigkeit des Windows Druckdiensts, indem Druckertreiber in Prozessen ausgeführt werden können, die von dem Prozess getrennt sind, in dem der Druckspooler ausgeführt wird. Unterstützung für die Druckertreiberisolation wurde in Windows 7 und Windows Server 2008 R2 gestartet. Eine App kann die Druckertreiberisolation im App-Manifest deklarieren, um sich vom Druckertreiber zu isolieren und seine Zuverlässigkeit zu verbessern. Das heißt, die App stürzt nicht ab, wenn der Druckertreiber einen Fehler aufweist.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

Gibt an, ob bildlauffähiges Bildlauf mit extrem hoher Auflösung aktiviert ist. **TRUE** gibt an, dass sie aktiviert ist. Sie verfügt über keine Attribute.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>MSIX

Gibt die Identitätsinformationen eines [MSIX-Pakets](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) mit geringer Dichte für die aktuelle Anwendung an. Dieses Element wird in Windows 10 Version 2004 und höher unterstützt.

Das **msix-Element** muss sich im Namespace `urn:schemas-microsoft-com:msix.v1` befinden. Sie verfügt über die attribute, die in der folgenden Tabelle angezeigt werden.

| Attribut   | Beschreibung                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Beschreibt die Herausgeberinformationen. Dieser Wert muss mit dem **Publisher** Attribut im [Identity-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) in Ihrem Sparsepaketmanifest übereinstimmen. |
| **packageName** | Beschreibt den Inhalt des Pakets. Dieser Wert muss mit dem **Name-Attribut** im [Identity-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) in Ihrem Sparsepaketmanifest übereinstimmen.    |
| **applicationId**    | Der eindeutige Bezeichner der Anwendung. Dieser Wert muss mit dem **Id-Attribut** im [Application-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-application) in Ihrem Sparsepaketmanifest übereinstimmen.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

Überschreibt die Standardheapimplementierungen für die zu verwendenden [Win32-Heap-APIs.](../Memory/heap-functions.md)

* Der Wert **SegmentHeap** gibt an, dass der Segmentheap verwendet wird. Segmentheap ist eine moderne Heapimplementierungen, die im Allgemeinen die Gesamtspeicherauslastung reduzieren. Dieses Element wird in Windows 10 Version 2004 (Build 19041) und höher unterstützt.
* Alle anderen Werte werden ignoriert.

Dieses Element weist keine Attribute auf.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Beispiel

Im Folgenden ist ein Beispiel für ein Anwendungsmanifest für eine Anwendung mit dem Namen MySampleApp.exe. Die Anwendung verwendet die SampleAssembly-Assembly nebeneinander.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
