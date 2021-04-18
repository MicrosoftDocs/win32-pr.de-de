---
description: Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Anwendungs Manifeste
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106365208"
---
# <a name="application-manifests"></a>Anwendungs Manifeste

Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll. Dabei sollte es sich um die gleichen Assemblyversionen handeln, die zum Testen der Anwendung verwendet wurden. Anwendungsmanifeste können auch Metadaten für private Anwendungsdateien beschreiben.

Eine umfassende Liste des XML-Schemas finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).

Anwendungs Manifeste verfügen über die folgenden Elemente und Attribute.

| Element                               | Attribute                | Erforderlich |
|---------------------------------------|---------------------------|----------|
| **Stadtverordneten**                          |                           | Ja      |
|                                       | **manifestVersion**       | Ja      |
| **NoInherit**                         |                           | Nein       |
| **AssemblyIdentity**                  |                           | Ja      |
|                                       | **type**                  | Ja      |
|                                       | **name**                  | Ja      |
|                                       | **language**              | Nein       |
|                                       | **processorArchitecture** | Nein       |
|                                       | **version**               | Ja      |
|                                       | **PublicKeyToken**        | Nein       |
| **glichkeits**                     |                           | Nein       |
| **application**                       |                           | Nein       |
| **supportedOS**                       | **Id**                    | Nein       |
| **"maxversiontested"**                  | **Id**                    | Nein       |
| **gkeit**                        |                           | Nein       |
| **dependentAssembly**                 |                           | Nein       |
| **datei**                              |                           | Nein       |
|                                       | **name**                  | Nein       |
|                                       | **HashAlg**               | Nein       |
|                                       | **hash**                  | Nein       |
| **activecodepage**                    |                           | Nein       |
| **automatische Erhöhung**                       |                           | Nein       |
| **wird deaktiviert**                    |                           | Nein       |
| **disablewindowfiltering**            |                           | Nein       |
| **dpiaware**                          |                           | Nein       |
| **dpiawareness**                      |                           | Nein       |
| **gdiskretihl**                        |                           | Nein       |
| **highresolutionscrollingaware**      |                           | Nein       |
| **longpathaware**                     |                           | Nein       |
| **printerdriverisolation**            |                           | Nein       |
| **ultrahighresolutionscrollingaware** |                           | Nein       |
| **msix**                              |                           | Nein       |
| **heaptype**                          |                           | Nein       |

## <a name="file-location"></a>Dateispeicherort

Anwendungs Manifeste sollten als Ressource in die exe-Datei oder DLL-Datei der Anwendung eingeschlossen werden.

Weitere Informationen finden Sie unter [Installieren](installing-side-by-side-assemblies.md)paralleler Assemblys.

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name einer Anwendungs Manifest-Datei ist der Name der ausführbaren Datei der Anwendung gefolgt von ". Manifest".

Beispielsweise würde ein Anwendungs Manifest, das auf example.exe oder example.dll verweist, die folgende Dateiname-Syntax verwenden. Wenn die Ressourcen-ID 1 ist, können Sie die <*Ressourcen-ID*> Feld weglassen.

**example.exe. <*Ressourcen-ID*>. Manifest**

**example.dll. <*Ressourcen-ID*>. Manifest**

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Groß-/Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, außer dem Wert des Type-Attributs.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>Assembly

Ein Containerelement. Das erste Unterelement muss ein **novererbungs** -oder **assemblyIdentity** -Element sein. Erforderlich.

Das **Assembly** -Element muss sich im Namespace "urn: Schemas-Microsoft-com: ASM. v1" befinden. Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.

Das **Assembly** -Element weist die folgenden Attribute auf.



| Attribut           | BESCHREIBUNG                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | Das **manifestVersion** -Attribut muss auf 1,0 festgelegt werden. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>NoInherit

Fügen Sie dieses Element in ein Anwendungs Manifest ein, um die aus dem Manifest generierten [Aktivierungs Kontexte](activation-contexts.md) mit dem Flag "No Erben" festzulegen. Wenn dieses Flag nicht in einem Aktivierungs Kontext festgelegt ist und der Aktivierungs Kontext aktiv ist, wird es von neuen Threads im gleichen Prozess, in Fenstern, in Fenster Prozeduren und [asynchronen Prozedur aufrufen](/windows/desktop/Sync/asynchronous-procedure-calls)geerbt. Durch Festlegen dieses Flags wird verhindert, dass das neue-Objekt den aktiven Kontext erbt.

Das **noerben** -Element ist optional und wird in der Regel ausgelassen. Die meisten Assemblys funktionieren nicht ordnungsgemäß mit einem Aktivierungs Kontext ohne Vererbung, da die Assembly explizit für die Verwaltung der Propagierung Ihres eigenen Aktivierungs Kontexts entworfen werden muss. Die Verwendung des **noerben** -Elements erfordert, dass alle abhängigen Assemblys, auf die das Anwendungs Manifest verweist, über ein **noerben** -Element in Ihrem Assemblymanifest verfügen [](assembly-manifests.md)

Wenn **novererbung** in einem Manifest verwendet wird, muss es das erste Unterelement des **Assembly** -Elements sein. Das **assemblyIdentity** -Element sollte direkt hinter dem **noerben** -Element stehen. Wenn **noerben** nicht verwendet wird, muss **assemblyIdentity** das erste untergeordnete Element des **Assembly** -Elements sein. Das **noerben** -Element weist keine untergeordneten Elemente auf. Es ist kein gültiges Element in [Assemblymanifesten](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Als erstes **Unterelement eines** **Assemblyelements beschreibt assemblyIdentity** die Anwendung, die dieses Anwendungs Manifest besitzt, und identifiziert Sie eindeutig. Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity** eine parallele Assembly, die für die Anwendung erforderlich ist. Beachten Sie, dass für jede Assembly, auf die im Anwendungs Manifest verwiesen wird, eine **assemblyIdentity** erforderlich ist, die exakt der **assemblyIdentity im eigenen Assemblymanifest** der referenzierten Assembly entspricht.

Das **assemblyIdentity** -Element verfügt über die folgenden Attribute. Sie hat keine unter Elemente.

| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Gibt den Anwendungs-oder Assemblytyp an. Der Wert muss Win32 und in Kleinbuchstaben sein. Erforderlich.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Benennt die Anwendung oder Assembly eindeutig. Verwenden Sie das folgende Format für den Namen: Organization.Division.Name. Beispiel: Microsoft. Windows. MySampleApp. Erforderlich.                                                                                                                                                                                                                                                               |
| **language**              | Identifiziert die Sprache der Anwendung oder Assembly. Dies ist optional. Wenn die Anwendung oder Assembly sprachspezifisch ist, geben Sie den Code der DHTML-Sprache an. Lassen Sie in der **Assemblyidentität** einer Anwendung, die für die weltweite Verwendung vorgesehen ist (Sprachneutral), das Language-Attribut aus.<br/> Legen Sie in einer **Assemblyidentität** einer Assembly, die für die weltweite Verwendung vorgesehen ist (Sprachneutral), den Wert der Sprache auf " \* " fest.<br/> |
| **processorArchitecture** | Gibt den Prozessor an. Gültige Werte sind `x86`, `amd64`, `arm` und `arm64`. Dies ist optional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Gibt die Anwendungs-oder Assemblyversion an. Verwenden Sie das vierteilige Versions Format: mmmmm. nnnnn. Ooooo. ppppp. Alle durch Zeiträume getrennten Teile können 0-65535 einschließlich sein. Weitere Informationen finden Sie unter [Assemblyversionen](assembly-versions.md). Erforderlich.                                                                                                                                                                        |
| **PublicKeyToken**        | Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Anwendung oder Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein. Erforderlich für alle freigegebenen parallelen Assemblys.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>Kompatibilität

Enthält mindestens eine **Anwendung**. Sie besitzt keine Attribute. Dies ist optional. Anwendungs Manifeste ohne Kompatibilitäts Element sind standardmäßig Windows Vista-Kompatibilität unter Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Enthält mindestens ein **SupportedOS** -Element. Ab Windows 10, Version 1903, kann es auch ein optionales **maxversiongeteteelement** enthalten. Sie besitzt keine Attribute. Dies ist optional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

Das **SupportedOS** -Element verfügt über das folgende Attribut. Sie hat keine unter Elemente.

| Attribut | BESCHREIBUNG   |
|-----------|-----------------------|
| **Id**    | Legen Sie das ID-Attribut auf **{e2011457-1546-43c5-a5fe-008deee3d3f0}** fest, um die Anwendung mit der Vista-Funktionalität auszuführen. Dadurch kann eine Anwendung, die für Windows Vista entwickelt wurde, unter einem späteren Betriebssystem ausgeführt werden. <br/> Legen Sie das ID-Attribut auf **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** fest, um die Anwendung mit der Windows 7-Funktionalität auszuführen.<br/> Anwendungen, die die Funktionen Windows Vista, Windows 7 und Windows 8 unterstützen, erfordern keine separaten Manifeste. Fügen Sie in diesem Fall die GUIDs für alle Windows-Betriebssysteme hinzu.<br/> Informationen zum Verhalten des **ID** -Attributs in Windows finden [Sie im Cookbook Windows 8 und Windows Server 2012 Compatibility](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Die folgenden GUIDs entsprechen den folgenden Betriebssystemen:<br/> **{8e0f 12-bsb3-4 FE8-b9a5-48sd50a15a9a}** -> Windows 10, Windows Server 2016 und Windows Server 2019<br/> **{1f676c76-80E1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 und Windows Server 2012 R2<br/> **{4a2s28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 und Windows Server 2012<br/> **{35138b9a-5d96-4f BD-8e2d-a2440225b93a}** -> Windows 7 und Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista und Windows Server 2008<br/> Sie können dies unter Windows 7 oder Windows 8. x testen, indem Sie Ressourcenmonitor (resmon) ausführen, auf die Registerkarte CPU klicken, mit der rechten Maustaste auf die Spalten Bezeichnungen, "Select column..." und dann auf "Operating System Context" klicken. Unter Windows 8. x können Sie diese Spalte auch im Task-Manager (Taskmgr) finden. Der Inhalt der Spalte zeigt den höchsten gefundenen Wert oder "Windows Vista" als Standardwert an. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>"maxversiontested"

Das **maxversiongetestete** -Element gibt die maximale Windows-Version an, für die die Anwendung getestet wurde. Diese soll von Desktop Anwendungen verwendet werden, die [XAML-Inseln](/windows/apps/desktop/modernize/xaml-islands) verwenden und nicht in einem msix-Paket bereitgestellt werden. Dieses Element wird in Windows 10, Version 1903 und höheren Versionen unterstützt.

Das **maxversiongetestete** -Element weist das folgende Attribut auf. Sie hat keine unter Elemente.

| Attribut | BESCHREIBUNG    |
|-----------|----------------|
| **Id**    | Legen Sie das ID-Attribut auf eine 4-teilige Versions Zeichenfolge fest, die die maximale Version von Windows angibt, mit der die Anwendung getestet wurde. Beispiel: "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Enthält mindestens eine **dependentAssembly**. Sie besitzt keine Attribute. Dies ist optional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Das erste Unterelement von **dependentAssembly** muss ein **assemblyIdentity** -Element sein, das eine parallele Assembly beschreibt, die für die Anwendung erforderlich ist. Jede **dependentAssembly** muss sich in genau einer **Abhängigkeit** befinden. Sie besitzt keine Attribute.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

Gibt die Dateien an, die für die Anwendung privat sind. Dies ist optional.

Das **File** -Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.



| Attribut   | BESCHREIBUNG                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Der Name der Datei. Beispielsweise Comctl32.dll.                                                            |
| **HashAlg** | Der Algorithmus, der zum Erstellen eines Hashwerts der Datei verwendet wird. Dieser Wert muss SHA1 lauten.                                 |
| **hash**    | Ein Hash der Datei, auf die nach Name verwiesen wird. Eine hexadezimale Zeichenfolge der Länge, abhängig vom Hash Algorithmus. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activecodepage

Erzwingen Sie, dass ein Prozess UTF-8 als Prozess Codepage verwendet.

**activecodepage** wurde in Windows, Version 1903 (Mai 2019 Update) hinzugefügt. Sie können diese Eigenschaft deklarieren und für frühere Windows-Builds ausführen/ausführen, aber Sie müssen die Legacy-Code Page Erkennung und-Konvertierung wie gewohnt behandeln. Weitere Informationen finden Sie [unter Verwenden der UTF-8-Codepage](/windows/uwp/design/globalizing/use-utf8-code-page) .

Dieses Element weist keine Attribute auf. **UTF-8** ist nur ein gültiger Wert für das **activecodepage** -Element.

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

### <a name="autoelevate"></a>automatische Erhöhung

Gibt an, ob die automatische Erhöhung aktiviert ist. **True** gibt an, dass es aktiviert ist. Sie besitzt keine Attribute.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>wird deaktiviert

Gibt an, ob das Festlegen von Benutzeroberflächen Elementen ein Design deaktiviert ist. **True** weist auf deaktiviert hin. Sie besitzt keine Attribute.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disablewindowfiltering

Gibt an, ob die Fenster Filterung deaktiviert werden soll. **True** deaktiviert die Fenster Filterung, sodass Sie die immersiven Fenster vom Desktop aufzählen können. **disablewindowfiltering** wurde in Windows 8 hinzugefügt und weist keine Attribute auf.

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

### <a name="dpiaware"></a>dpiaware

Gibt an, ob der aktuelle Prozess Punkte pro Zoll (dpi) unterstützt.

**Windows 10, Version 1607:** Das **dpiaware** -Element wird ignoriert, wenn das **dpiawareness** -Element vorhanden ist. Wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten, können Sie beide Elemente in ein Manifest einschließen.

In der folgenden Tabelle wird das Verhalten beschrieben, das sich basierend auf dem vorhanden sein des Elements **dpiaware** und dem darin enthaltenen Text ergibt. Bei dem Text im-Element wird die Groß-/Kleinschreibung nicht beachtet.

| Status des **dpiaware** -Elements | BESCHREIBUNG     |
|-----------------------------------|---------|
| „Absent“                            | Im aktuellen Prozess ist dpi standardmäßig nicht bekannt. Sie können diese Einstellung Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.                                                                                                                                                            |
| Enthält "true"                   | Der aktuelle Prozess ist System-dpi-fähig.                                                                                                                                                                                                                                                                                                                                                          |
| Enthält "false"                  | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist dpi-Wert, und Sie können diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.<br/> |
| Enthält "true/pm".                | **Windows Vista, Windows 7 und Windows 8:** Der aktuelle Prozess ist System-dpi-fähig.<br/> **Windows 8.1 und Windows 10:** Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.<br/>                                                                                                                                                                                                          |
| Enthält "pro Monitor"            | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.<br/>                                                                                                                                                                                      |
| Enthält eine beliebige andere Zeichenfolge         | **Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.<br/> **Windows 8.1 und Windows 10:** Der aktuelle Prozess ist dpi-Wert, und Sie können diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.<br/> |

Weitere Informationen zu den dpi-Einstellungen finden Sie unter [Vergleich der dpi-Bekanntheits Grade](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

**dpiaware** weist keine Attribute auf.

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

### <a name="dpiawareness"></a>dpiawareness

Gibt an, ob der aktuelle Prozess Punkte pro Zoll (dpi) unterstützt.

Die Mindestversion des Betriebssystems, das das **dpiawareness** -Element unterstützt, ist Windows 10, Version 1607. Für Versionen, die das **dpiawareness** -Element unterstützen, überschreibt **dpiawareness** das **dpiaware** -Element. Wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten, können Sie beide Elemente in ein Manifest einschließen.

Das **dpiawareness** -Element kann ein einzelnes Element oder eine Liste mit durch Trennzeichen getrennten Elementen enthalten. Im letzteren Fall wird das erste (am weitesten links stehende) Element in der Liste verwendet, das vom Betriebssystem erkannt wird. Auf diese Weise können Sie verschiedene Verhalten angeben, die in zukünftigen Windows-Betriebssystemversionen unterstützt werden.

In der folgenden Tabelle wird das Verhalten beschrieben, das sich auf der Grundlage des Vorhandenseins des **dpiawareness** -Elements und des darin enthaltenen Texts in seinem am weitesten links erkannten Element ergibt. Bei dem Text im-Element wird die Groß-/Kleinschreibung nicht beachtet.

| Status des **dpiawareness** -Elements:        | BESCHREIBUNG                          |
|-----------------------------------------|-------------------------------------------|
| Das Element fehlt.                       | Das **dpiaware** -Element gibt an, ob der Prozess dpi-fähig ist.                                                                                                                                                                   |
| Enthält keine erkannten Elemente            | Im aktuellen Prozess ist dpi standardmäßig nicht bekannt. Sie können diese Einstellung Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen. |
| Das erste erkannte Element ist "System".       | Der aktuelle Prozess ist System-dpi-fähig.                                                                                                                                                                                               |
| Das erste erkannte Element ist "permonitor".   | Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.                                                                                                                                                                                          |
| Das erste erkannte Element ist "permonitorv2". | Der aktuelle Prozess verwendet den dpi-Kontext für den dpi-Kontext pro Monitor. Dieses Element wird nur unter Windows 10, Version 1703 oder höher, erkannt.                                                                                              |
| Das erste erkannte Element ist "nicht bekannt".      | Beim aktuellen Prozess ist dpi nicht bekannt. Sie **können** diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.      |

Weitere Informationen zu den von diesem Element unterstützten dpi-Informationen finden Sie unter dpi-Informationen und [ \_ \_ Kontext](/windows/desktop/hidpi/dpi-awareness-context)für dpi-Informationen. [ \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness)

**dpiawareness** weist keine Attribute auf.

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

### <a name="gdiscaling"></a>gdiskretihl

Gibt an, ob GDI-Skalierung aktiviert ist. Die Mindestversion des Betriebssystems, das das **gdiscement** -Element unterstützt, ist Windows 10, Version 1703.

Das GDI-Framework (Graphics Device Interface) kann die DPI-Skalierung auf primitive und Text pro Monitor anwenden, ohne dass Aktualisierungen an der Anwendung selbst erfolgen. Dies kann für GDI-Anwendungen nützlich sein, die nicht mehr aktiv aktualisiert werden.

Nicht Vektorgrafiken (z. b. Bitmaps, Symbole oder Symbolleisten) können nicht von diesem Element skaliert werden. Darüber hinaus können Grafiken und Text, die in Bitmaps angezeigt werden, die dynamisch von Anwendungen erstellt werden, auch nicht von diesem Element skaliert werden.

**True** gibt an, dass dieses Element aktiviert ist. Sie besitzt keine Attribute.


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

### <a name="highresolutionscrollingaware"></a>highresolutionscrollingaware

Gibt an, ob das hochauflösende Scrollen aktiviert ist. **True** gibt an, dass es aktiviert ist. Sie besitzt keine Attribute.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longpathaware

Aktiviert lange Pfade, die **MAX_PATH** Länge überschreiten. Dieses Element wird in Windows 10, Version 1607 und höher, unterstützt. [hier finden Sie weitere Informationen](../fileio/maximum-file-path-limitation.md)

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

### <a name="printerdriverisolation"></a>printerdriverisolation

Gibt an, ob die Druckertreiber Isolation aktiviert ist. **True** gibt an, dass es aktiviert ist. Sie besitzt keine Attribute. Die Druckertreiber Isolation verbessert die Zuverlässigkeit des Windows-Druck Diensts, indem Druckertreiber in Prozessen ausgeführt werden können, die von dem Prozess getrennt sind, in dem der Druck Spooler ausgeführt wird. Unterstützung für die Druckertreiber Isolation in Windows 7 und Windows Server 2008 R2. Eine APP kann die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um sich selbst vom Druckertreiber zu isolieren und seine Zuverlässigkeit zu verbessern. Das heißt, die APP stürzt nicht ab, wenn der Druckertreiber einen Fehler aufweist.


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

### <a name="ultrahighresolutionscrollingaware"></a>ultrahighresolutionscrollingaware

Gibt an, ob die hochauflösende Bild lauffunktion aktiviert ist. **True** gibt an, dass es aktiviert ist. Sie besitzt keine Attribute.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>MSIX

Gibt die Identitätsinformationen eines [sparsemsix-Pakets](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) für die aktuelle Anwendung an. Dieses Element wird in Windows 10, Version 2004 und höheren Versionen unterstützt.

Das **msix** -Element muss sich im-Namespace befinden `urn:schemas-microsoft-com:msix.v1` . Die Attribute sind in der folgenden Tabelle aufgeführt.

| Attribut   | BESCHREIBUNG                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Beschreibt die Verleger Informationen. Dieser Wert muss mit dem **Verleger** Attribut im [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) -Element in Ihrem Paket mit geringer Dichte identisch sein. |
| **packageName** | Beschreibt den Inhalt des Pakets. Dieser Wert muss mit dem **Name** -Attribut im [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) -Element im Sparse-Paket Manifest identisch sein.    |
| **applicationId**    | Der eindeutige Bezeichner der Anwendung. Dieser Wert muss mit dem **ID** -Attribut im [Anwendungs](/uwp/schemas/appxpackage/uapmanifestschema/element-application) Element im Sparse-Paket Manifest identisch sein.  |

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

### <a name="heaptype"></a>heaptype

Überschreibt die standardmäßige Heap Implementierung für die zu verwendenden [Win32-Heap-APIs](../Memory/heap-functions.md) .

* Der Wert **segmentheiap** gibt an, dass der Segment Heap verwendet wird. Der Segment Heap ist eine moderne Heap Implementierung, die in der Regel die Gesamtspeicher Auslastung reduziert. Dieses Element wird in Windows 10, Version 2004 (Build 19041) und höher unterstützt.
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

Im folgenden finden Sie ein Beispiel für ein Anwendungs Manifest für eine Anwendung mit dem Namen MySampleApp.exe. Die Anwendung verwendet die parallele Assembly von SampleAssembly.

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
