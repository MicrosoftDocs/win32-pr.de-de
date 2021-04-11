---
description: Eine Anwendungs Konfigurationsdatei ist eine XML-Datei zum Steuern der Assemblybindung.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Anwendungskonfigurationsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128833"
---
# <a name="application-configuration-files"></a>Anwendungskonfigurationsdateien

Eine Anwendungs Konfigurationsdatei ist eine XML-Datei zum Steuern der Assemblybindung. Es kann eine Anwendung von der Verwendung einer Version einer parallelen Assembly zu einer anderen Version derselben Assembly umleiten. Dies wird [pro Anwendungskonfiguration](per-application-configuration.md)bezeichnet. Eine Anwendungs Konfigurationsdatei gilt nur für ein bestimmtes Anwendungs Manifest und abhängige Assemblys. Isolierte Komponenten, die mit einem eingebetteten isolationaware Manifest-Ressourcen-ID-Manifest kompiliert werden, \_ \_ \_ erfordern eine separate Anwendungs Konfigurationsdatei. Manifeste, die mit " [**kreateactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) " verwaltet werden, benötigen eine separate Anwendungs Konfigurationsdatei

Die durch eine Anwendungs Konfigurationsdatei angegebene Umleitung kann die von [Anwendungs Manifesten](application-manifests.md) und [Verleger Konfigurationsdateien](publisher-configuration-files.md)angegebenen Assemblyversionen außer Kraft setzen. Wenn eine Verleger Konfigurationsdatei z. b. angibt, dass alle Verweise auf eine Assembly von Version 1.0.0.0 zu 1.1.0.0 umgeleitet werden, kann eine Anwendungs Konfigurationsdatei verwendet werden, um eine bestimmte Anwendung zur Verwendung von Version 1.0.0.0 umzuleiten. Eine Anwendungs Konfigurationsdatei gilt nur für das angegebene Anwendungs Manifest und abhängige Assemblys.

Eine umfassende Liste des XML-Schemas finden Sie unter [Schema der Anwendungs Konfigurationsdatei](application-configuration-file-schema.md).

Anwendungs Konfigurationsdateien haben die Elemente und Attribute, die in der folgenden Tabelle aufgeführt sind.



| Element               | Attribute                | Erforderlich |
|-----------------------|---------------------------|----------|
| **configuration**     |                           | Ja      |
| **windows**           |                           | Ja      |
| **publisherPolicy**   |                           | Ja      |
|                       | **Apply**                 | Ja      |
| **Laufzeit**           |                           | Nein       |
| **assemblyBinding**   |                           | Ja      |
| **Test**           |                           | Nein       |
|                       | **privatePath**           | Ja      |
| **gkeit**        |                           | Nein       |
| **dependentAssembly** |                           | Ja      |
| **AssemblyIdentity**  |                           | Ja      |
|                       | **type**                  | Ja      |
|                       | **name**                  | Ja      |
|                       | **language**              | Nein       |
|                       | **processorArchitecture** | Ja      |
|                       | **version**               | Ja      |
|                       | **PublicKeyToken**        | Nein       |
| **bindingRedirect**   |                           | Ja      |
|                       | **OldVersion**            | Ja      |
|                       | **NewVersion**            | Ja      |



 

## <a name="file-location"></a>Dateispeicherort

Anwendungs Konfigurationsdateien müssen am gleichen Speicherort wie das Anwendungs [Manifest](application-manifests.md)der Anwendung installiert werden.

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name einer Anwendungs Konfigurationsdatei ist der Name der ausführbaren Datei der Anwendung, gefolgt von. config.

Beispielsweise würde eine Anwendungs Konfigurationsdatei, die auf Example.exe oder Example.dll verweist, die im folgenden Beispiel gezeigte Syntax für den Dateinamen verwenden. Sie können das Feld für die Ressourcen- *ID* <> weglassen, wenn die Konfigurationsdatei als separate Datei installiert wird oder wenn die Ressourcen-ID 1 lautet.

**example.exe. <*Ressourcen-ID* # C1.config**

**example.dll. <*Ressourcen-ID* # C1.config**

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Groß-/Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird nicht zwischen Groß-und Kleinschreibung unterbunden, außer dem Wert des Type-Attributs.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>Konfiguration

Ein Containerelement für die **Windows** -und **Runtime** -Elemente einer Anwendungs Konfigurationsdatei. Erforderlich.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>Windows

Schließt die Teile der Anwendungs Konfigurationsdatei ein, die für die Umleitung von Win32-Assemblys gelten.

> [!Note]  
> Der Autor einer Anwendung sollte keine Konfigurationsdatei mit einem **Windows** -Unterelement als Teil Ihrer Anwendung einschließen. Dies ist möglicherweise zulässig, wenn der einzige Zweck der Konfigurationsdatei darin besteht, die **privatePath** -Funktionalität eines **probingelements** zu aktivieren. Das **probingelement** ist auf Systemen vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Gibt an, ob Herausgeber Richtlinien angewendet werden sollen.

Dieses Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.



| Attribut | BESCHREIBUNG                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **Apply** | Mit dem Wert "yes" wird die Herausgeber Richtlinie angewendet. Dies ist die Standardeinstellung. Der Wert "No" wendet die Herausgeber Richtlinie nicht an. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>Laufzeit

Schließt die Teile der Anwendungs Konfigurationsdatei ein, die für die Umleitung von .NET-Assemblys gelten.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Enthält die Umleitungs Informationen für die Anwendung und die Assembly, auf die sich diese Anwendungs Konfigurationsdatei auswirkt. Das erste untergeordnete Element von **assemblyBinding** muss eine **assemblyIdentity** sein, die die Anwendung identifiziert.

Ab Windows Server 2008 R2 und Windows 7 kann ein **assemblyBinding** -Element ein **probingsubelement** enthalten.

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>Prüfen

Ein optionales Unterelement eines **assemblyBinding** -Elements, das die Suche nach Assemblys in weitere Verzeichnisse erweitert. Die zusätzlichen Verzeichnisse müssen keine Unterverzeichnisse des Verzeichnisses der Assembly sein.

> [!Note]  
> Dieses Element ist auf Systemen vor Windows Server 2008 R2 und Windows 7 nicht verfügbar und kann nur innerhalb eines **Windows** -Elements verwendet werden.

Dieses Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.

| Attribut       | BESCHREIBUNG                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Gibt die [relativen Pfade](/windows/desktop/FileIO/naming-a-file) der Unterverzeichnisse des Basisverzeichnisses der Anwendung an, die Assemblys enthalten können. Es können maximal neun Unterverzeichnis Pfade angegeben werden. Begrenzen der einzelnen Unterverzeichnis Pfade mit einem Semikolon. |

Sie können den Doppelpunkte-sonderspezifizierer in einem Pfad verwenden, um das übergeordnete Verzeichnis des aktuellen Verzeichnisses anzugeben. Es können nicht mehr als zwei Ebenen oberhalb des aktuellen Verzeichnisses mit doppelten Punkten angegeben werden. Verwenden Sie keine dreifachen Punkte. Beispielsweise prüft eine Anwendung, die das **folgende Test** Element verwendet, zusätzliche Verzeichnisse für eine Assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Ein Containerelement für mindestens eine **dependentAssembly**. Jede **dependentAssembly** kann sich in genau einer **Abhängigkeit** befinden. Dieses Element weist keine Attribute auf. Dies ist optional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Beim ersten Unterelement muss es sich um ein **assemblyIdentity** -Element handeln, das die parallele Assembly identifiziert, die von der Anwendungs Konfigurationsdatei umgeleitet wird. Eine **dependentAssembly** weist keine Attribute auf.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Als erstes Unterelement eines **assemblyBinding** -Elements beschreibt **assemblyIdentity** eine Anwendung und identifiziert diese eindeutig. Die Anwendungs Konfigurationsdatei leitet die Bindung dieser Anwendung an parallele Assemblys um. Beispielsweise gibt die folgende **assemblyIdentity** an, dass sich die Anwendungs Konfigurationsdatei auf die Bindung der Anwendung MySampleApp an parallele Assemblys auswirkt. Die Assemblys, die umgeleitet werden, werden in einer **dependentAssembly** identifiziert.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity** eine parallele Assembly, von der die Anwendung abhängt. Die Anwendungs Konfigurationsdatei konfiguriert die Identität dieser erforderlichen Assembly neu. Beispielsweise wird durch die folgende **assemblyIdentity** und **bindingRedirect** eine Abhängigkeit von Version 2.0.0.0 auf Version 2.1.0.0 neu konfiguriert.

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

Beachten Sie, dass jede in einer **dependentAssembly** enthaltene **assemblyIdentity** genau mit der **assemblyIdentity im eigenen Assemblymanifest** der Assembly übereinstimmen muss. [](assembly-manifests.md)

Das **assemblyIdentity** -Element verfügt über die folgenden Attribute. Sie hat keine unter Elemente.

| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Der Wert muss Win32 (Kleinbuchstaben) sein. Erforderlich.                                                                                                                                                                                                                                                                      |
| **name**                  | Das Attribut Name identifiziert die Anwendung, die von der Anwendungs Konfigurationsdatei oder der Assembly, die umgeleitet wird, betroffen ist. Verwenden Sie das folgende Format für den Namen: Organization.Division.Name. Erforderlich. Beispiel: Microsoft. Windows. MySampleApp oder Microsoft. Windows. mysampleasm.<br/>            |
| **language**              | Gibt die Sprache an. Dies ist optional. Geben Sie für eine **assemblyIdentity** , die auf eine Assembly verweist, den DHTML-Sprachcode an, wenn die Assembly sprachspezifisch ist. Wenn die Assembly für den weltweiten Gebrauch (Sprachneutral) verwendet wird, legen Sie den Wert auf " \* " fest.<br/>                                                            |
| **processorArchitecture** | Gibt den Prozessor an, auf dem die Anwendung ausgeführt wird.                                                                                                                                                                                                                                                                     |
| **version**               | Gibt die Version der Anwendung oder Assembly an. Verwenden Sie die vierteilige Versions Syntax: mmmm. nnnn. oooo. pppp. Erforderlich.                                                                                                                                                                                                   |
| **PublicKeyToken**        | Für eine **assemblyIdentity** , die auf eine Assembly verweist, eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein. Erforderlich für alle freigegebenen parallelen Assemblys. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

Das **bindingRedirect** -Element enthält Umleitungs Informationen für die Bindung der Assembly. Alle **bindingRedirect** -Elemente müssen in genau einem **dependentAssembly**-Verzeichnis enthalten sein. Die vierteilige Versions Syntax der neuen Version und der alten Version müssen die gleichen Haupt-und neben Versionen angeben.

Dieses Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.

| Attribut      | BESCHREIBUNG                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OldVersion** | Gibt die Assemblyversion an, die überschrieben und umgeleitet wird. Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn. Geben Sie einen Bereich von Versionen mit einem Bindestrich ohne Leerzeichen an. Beispielsweise 2.14.3.0 oder 2.14.3.0 2.16.0.0. Erforderlich. |
| **NewVersion** | Gibt die Version der Ersetzungs-Assembly an. Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Bemerkungen

In Anwendungs Konfigurationsdateien werden keine Dateien angegeben.

## <a name="example"></a>Beispiel

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
