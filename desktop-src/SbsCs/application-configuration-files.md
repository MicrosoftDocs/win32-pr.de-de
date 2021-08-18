---
description: Eine Anwendungskonfigurationsdatei ist eine XML-Datei, die zum Steuern der Assemblybindung verwendet wird.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Anwendungskonfigurationsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf4b22d3710c0dd38e83f827a175ad591309f22ab8ac2d81e93438f27d07dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142523"
---
# <a name="application-configuration-files"></a>Anwendungskonfigurationsdateien

Eine Anwendungskonfigurationsdatei ist eine XML-Datei, die zum Steuern der Assemblybindung verwendet wird. Sie kann eine Anwendung von der Verwendung einer Version einer gleichzeitigen Assembly zu einer anderen Version derselben Assembly umleiten. Dies wird [anwendungsspezifische Konfiguration genannt.](per-application-configuration.md) Eine Anwendungskonfigurationsdatei gilt nur für ein bestimmtes Anwendungsmanifest und abhängige Assemblys. Isolierte Komponenten, die mit einem eingebetteten ISOLATIONAWARE \_ MANIFEST \_ RESOURCE \_ ID-Manifest kompiliert werden, erfordern eine separate Anwendungskonfigurationsdatei. Manifeste, die mit [**CreateActCtx verwaltet**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) werden, erfordern eine separate Anwendungskonfigurationsdatei.

Die durch eine [Anwendungskonfigurationsdatei](application-manifests.md) angegebene Umleitung kann die von Anwendungsmanifesten und Herausgeberkonfigurationsdateien angegebenen [Assemblyversionen überschreiben.](publisher-configuration-files.md) Wenn eine Herausgeberkonfigurationsdatei beispielsweise angibt, dass alle Verweise auf eine Assembly von Version 1.0.0.0 zu 1.1.0.0 umgeleitet werden, kann eine Anwendungskonfigurationsdatei verwendet werden, um eine bestimmte Anwendung zur Verwendung von Version 1.0.0.0 umzuleiten. Eine Anwendungskonfigurationsdatei gilt nur für das angegebene Anwendungsmanifest und abhängige Assemblys.

Eine vollständige Liste des XML-Schemas finden Sie unter [Schema der Anwendungskonfigurationsdatei.](application-configuration-file-schema.md)

Anwendungskonfigurationsdateien verfügen über die in der folgenden Tabelle gezeigten Elemente und Attribute.



| Element               | Attribute                | Erforderlich |
|-----------------------|---------------------------|----------|
| **configuration**     |                           | Ja      |
| **windows**           |                           | Ja      |
| **publisherPolicy**   |                           | Ja      |
|                       | **Anwenden**                 | Ja      |
| **Laufzeit**           |                           | Nein       |
| **assemblyBinding**   |                           | Ja      |
| **Sondieren**           |                           | Nein       |
|                       | **Privatepath**           | Ja      |
| **Abhängigkeit**        |                           | Nein       |
| **Dependentassembly** |                           | Ja      |
| **Assemblyidentity**  |                           | Ja      |
|                       | **type**                  | Ja      |
|                       | **name**                  | Ja      |
|                       | **language**              | Nein       |
|                       | **processorArchitecture** | Ja      |
|                       | **version**               | Ja      |
|                       | **Publickeytoken**        | Nein       |
| **bindingRedirect**   |                           | Ja      |
|                       | **oldVersion**            | Ja      |
|                       | **Newversion**            | Ja      |



 

## <a name="file-location"></a>Speicherort

Anwendungskonfigurationsdateien müssen am gleichen Speicherort wie das Anwendungsmanifest der [Anwendung installiert werden.](application-manifests.md)

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name einer Anwendungskonfigurationsdatei ist der Name der ausführbaren Anwendungsdatei, gefolgt von .config.

Beispielsweise würde eine Anwendungskonfigurationsdatei, die auf Example.exe oder Example.dll, die im folgenden Beispiel gezeigte Dateinamensyntax verwenden. Sie können das Feld für <*Ressourcen-ID* weglassen> wenn Sie die Konfigurationsdatei als separate Datei installieren oder wenn die Ressourcen-ID 1 ist.

***example.exe.<-Ressourcen-ID*>.config**

***example.dll.<-Ressourcen-ID*>.config**

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme des Werts des Typattributs.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>Konfiguration

Ein Containerelement für die **Windows- und** **Runtimeelemente** einer Anwendungskonfigurationsdatei. Erforderlich.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>Windows

Enthält die Teile der Anwendungskonfigurationsdatei, die für die Umleitung von Win32-Assemblys gelten.

> [!Note]  
> Der Autor einer Anwendung darf keine Konfigurationsdatei mit einem **Windows-Unterelement** als Teil der Anwendung enthalten. Dies kann zulässig sein, wenn der einzige Zweck der Konfigurationsdatei das Aktivieren der **privatePath-Funktionalität** eines **Suchelements** ist. Das **Element probing** ist auf Systemen vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Gibt an, ob die Herausgeberrichtlinie angewendet werden soll.

Dieses Element enthält die in der folgenden Tabelle gezeigten Attribute.



| attribute | Beschreibung                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **Anwenden** | Der Wert "Yes" wendet die Herausgeberrichtlinie an. Dies ist die Standardeinstellung. Der Wert "no" gilt nicht für die Herausgeberrichtlinie. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>Laufzeit

Enthält die Teile der Anwendungskonfigurationsdatei, die für die Umleitung von .NET-Assemblys gelten.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Enthält die Umleitungsinformationen für die Anwendung und die Assembly, die von dieser Anwendungskonfigurationsdatei betroffen sind. Das erste Unterelement von **assemblyBinding** muss eine **assemblyIdentity** sein, die die Anwendung identifiziert.

Ab Windows Server 2008 R2 und Windows 7 kann ein **assemblyBinding-Element** ein **Untergeordnetes** Element für die Probe enthalten.

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>Prüfen

Ein optionales Unterelement eines **assemblyBinding-Elements,** das die Suche nach Assemblys in zusätzliche Verzeichnisse erweitert. Die zusätzlichen Verzeichnisse müssen keine Unterverzeichnisse des Verzeichnisses der Assembly sein.

> [!Note]  
> Dieses Element ist auf Systemen vor Windows Server 2008 R2 und Windows 7 nicht verfügbar und kann nur innerhalb eines **Windows-Elements verwendet** werden.

Dieses Element enthält die in der folgenden Tabelle gezeigten Attribute.

| attribute       | Beschreibung                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Privatepath** | Gibt die [relativen Pfade von](/windows/desktop/FileIO/naming-a-file) Unterverzeichnissen des Basisverzeichnisses der Anwendung an, die Assemblys enthalten können. Es können maximal neun Unterverzeichnispfade angegeben werden. Begrenzen Sie jeden Unterverzeichnispfad durch ein Semikolon. |

Sie können den speziellen Spezifizierer mit doppelten Punkten in einem Pfad verwenden, um das übergeordnete Verzeichnis des aktuellen Verzeichnisses zu kennzeichnen. Es können nicht mehr als zwei Ebenen oberhalb des aktuellen Verzeichnisses mit doppelten Punkten angegeben werden. Verwenden Sie keine drei Punkte. Beispielsweise überprüft eine Anwendung, die das folgende **Testelement** verwendet, zusätzliche Verzeichnisse für eine Assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Ein Containerelement für mindestens ein **dependentAssembly-Element.** Jede **dependentAssembly** kann sich innerhalb genau einer **Abhängigkeit** befinden. Dieses Element weist keine Attribute auf. Optional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Das erste Unterelement muss ein **assemblyIdentity-Element** sein, das die von der Anwendungskonfigurationsdatei umgeleitete side-by-side-Assembly identifiziert. Eine **dependentAssembly** verfügt über keine Attribute.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Als erstes Unterelement eines **assemblyBinding-Elements** beschreibt **assemblyIdentity** eine Anwendung und identifiziert sie eindeutig. Die Anwendungskonfigurationsdatei leitet die Bindung dieser Anwendung an nebeneinander ausgeführte Assemblys um. Die folgende **assemblyIdentity gibt z. B.** an, dass die Anwendungskonfigurationsdatei die Bindung der Anwendung mysampleApp an nebeneinander seitige Assemblys beeinflusst. Die Assemblys, die umgeleitet werden, werden in einer **dependentAssembly** identifiziert.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Als erstes Unterelement eines **dependentAssembly-Elements** beschreibt **assemblyIdentity** eine nebengeschaltete Assembly, von der die Anwendung abhängt. Die Anwendungskonfigurationsdatei konfiguriert die Identität dieser erforderlichen Assembly neu. Mit der folgenden **assemblyIdentity** und **bindingRedirect** wird beispielsweise eine Abhängigkeit von Microsoft neu konfiguriert. Windows. SampleAssembly von Version 2.0.0.0 bis Version 2.1.0.0.

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

Beachten Sie, dass jede **assemblyIdentity,** die in einer **dependentAssembly** enthalten ist, genau mit **assemblyIdentity** im eigenen [Assemblymanifest](assembly-manifests.md)der Assembly übereinstimmen muss.

Das **assemblyIdentity-Element** verfügt über die folgenden Attribute. Sie verfügt über keine Unterelemente.

| attribute                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Der Wert muss win32 (Kleinbuchstaben) sein. Erforderlich.                                                                                                                                                                                                                                                                      |
| **name**                  | Das Name-Attribut identifiziert die Anwendung, die von der Anwendungskonfigurationsdatei oder der Assembly betroffen ist, die umgeleitet wird. Verwenden Sie das folgende Format für den Namen: Organization.Division.Name. Erforderlich. Beispiel: Microsoft. Windows. MysampleApp oder Microsoft. Windows. MysampleAsm.<br/>            |
| **language**              | Identifiziert die Sprache. Optional. Geben Sie für eine **assemblyIdentity,** die auf eine Assembly verweist, den DHTML-Sprachcode an, wenn die Assembly sprachspezifisch ist. Wenn die Assembly für die weltweite Verwendung vorgesehen ist (sprachneutral), legen Sie den Wert auf " \* " fest.<br/>                                                            |
| **processorArchitecture** | Gibt den Prozessor an, auf dem die Anwendung ausgeführt wird.                                                                                                                                                                                                                                                                     |
| **version**               | Gibt die Version der Anwendung oder Assembly an. Verwenden Sie die vierteilige Versionssyntax mmmm.nnnn.oooo.ppp. Erforderlich.                                                                                                                                                                                                   |
| **Publickeytoken**        | Für eine **assemblyIdentity,** die auf eine Assembly verweist, eine Hexadezimalzeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der zum Signieren des Katalogs verwendete öffentliche Schlüssel muss 2048 Bit oder höher sein. Erforderlich für alle freigegebenen nebeneinander verwendeten Assemblys. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

Das **bindingRedirect-Element** enthält Umleitungsinformationen für die Bindung der Assembly. Jedes **bindingRedirect** muss in genau einem **dependentAssembly** enthalten sein. In der vierteiligen Versionssyntax der neuen version und der alten Version müssen die gleichen Haupt- und Nebenversionen angegeben werden.

Dieses Element verfügt über die in der folgenden Tabelle gezeigten Attribute.

| attribute      | Beschreibung                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Gibt die Assemblyversion an, die überschrieben und umgeleitet wird. Verwenden Sie die vierteilige Versionssyntax nnnnn.nnnnn.nnnnn.nnnnn. Geben Sie einen Bereich von Versionen durch einen Bindestrich ohne Leerzeichen an. Beispiel: 2.14.3.0 oder 2.14.3.0 2.16.0.0. Erforderlich. |
| **Newversion** | Gibt die Version der Ersatzassembly an. Verwenden Sie die vierteilige Versionssyntax nnnnn.nnnnn.nnnnn.nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Hinweise

Anwendungskonfigurationsdateien geben keine Dateien an.

## <a name="example"></a>Beispiel

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
