---
description: Eine Verleger Konfigurationsdatei ist eine XML-Datei, die Anwendungen und Assemblys global von der Verwendung einer Version einer parallelen Assembly zu einer anderen Version derselben Assembly umleitet.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Verleger Konfigurationsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867888"
---
# <a name="publisher-configuration-files"></a>Verleger Konfigurationsdateien

Eine Verleger Konfigurationsdatei ist eine XML-Datei, die Anwendungen und Assemblys global von der Verwendung einer Version einer parallelen Assembly zu einer anderen Version derselben Assembly umleitet. In der Regel gibt der Verleger der Assembly ein kompatibles Update oder eine Sicherheitskorrektur pro Assembly aus, indem eine zu installierende Verleger Konfigurationsdatei zusammen mit einem Service Pack Update ausgegeben wird. Dies wird als [Verleger Konfiguration](publisher-configuration.md)bezeichnet. Weitere Informationen zu diesem [Konfigurationstyp](configuration.md) finden Sie unter Verleger Konfiguration.

Die Verleger Konfigurationsdateien haben die folgenden Elemente und Attribute. Eine umfassende Liste des XML-Schemas finden Sie unter [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md).



| Element               | Attribute                | Erforderlich |
|-----------------------|---------------------------|----------|
| **Stadtverordneten**          |                           | Ja      |
|                       | **manifestVersion**       | Ja      |
| **AssemblyIdentity**  |                           | Ja      |
|                       | **type**                  | Ja      |
|                       | **name**                  | Ja      |
|                       | **language**              | Nein       |
|                       | **processorArchitecture** | Nein       |
|                       | **version**               | Ja      |
|                       | **PublicKeyToken**        | Nein       |
| **gkeit**        |                           | Nein       |
| **dependentAssembly** |                           | Nein       |
| **bindingRedirect**   |                           | Ja      |
|                       | **OldVersion**            | Ja      |
|                       | **NewVersion**            | Ja      |



 

## <a name="file-location"></a>Dateispeicherort

Die Verleger Konfigurationsdateien müssen im Ordner WinSxS installiert sein. Sie werden normalerweise als separate Datei installiert, aber Verleger Konfigurationsdateien können auch als Ressource in eine DLL eingeschlossen werden. Eine Verleger Konfigurationsdatei kann nicht als Ressource in eine exe-Datei eingeschlossen werden. Eine exe-Datei kann ein [Anwendungs Manifest](application-manifests.md) als Ressource enthalten.

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Dateiname einer Verleger Konfigurationsdatei hat die Formular *Richtlinie*. *Haupt* Version. *neben* Version. *AssemblyName* , wobei " *Major* " und " *Minor* " auf die Haupt-und neben Teile der Assemblyversion verweisen, die betroffen ist. [](assembly-versions.md) *AssemblyName* verweist auf den Namen der Assembly.

Eine Verleger Konfigurationsdatei für Version 6,0 der Microsoft. Windows. Common-Controls-Assembly hätte z. b. den folgenden Namen:

<dl> Policy. 6.0. Microsoft. Windows. Common-Controls  
</dl>

Verwenden Sie keine Richtlinien Konfigurationsdateien, um die Haupt-oder neben Version einer Assembly zu erhöhen. Umleiten Sie z. b. Version 6.0.0.0 nicht zu 7.0.0.0 oder 6.1.0.0. Wenn eine Anwendung auf eine Assemblyversion, z. b. 6.0.0.0, verweist, prüft parallel, ob Richtlinien Konfigurationsdateien mit den angegebenen Haupt-und neben Versionen vorhanden sind, z. b. 6,0. Die Anwendung wird dann an eine andere Version der Assembly umgeleitet, z. b. 6.0.1.0. Wenn eine Verleger Konfigurationsdatei die Haupt-oder neben Version einer Assembly Inkremente erhöht, müssen bei der nachfolgenden Umleitung der Assembly möglicherweise mehrere Richtlinien Konfigurationsdateien ausgegeben werden.

## <a name="elements"></a>Elemente

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**Stadtverordneten**
</dt> <dd>

Ein Containerelement. Das erste untergeordnete Element muss eine **assemblyIdentity** sein. Erforderlich.

Das Assembly-Element muss sich im Namespace **urn: Schemas-Microsoft-com: ASM. v1** befinden. Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.

Das **Assembly** -Element weist die folgenden Attribute auf.



| Attribut           | BESCHREIBUNG                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | Das **manifestVersion** -Attribut muss auf 1,0 festgelegt werden. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**AssemblyIdentity**
</dt> <dd>

Beschreibt eine parallele Assembly und identifiziert diese eindeutig.

Als erstes Unterelement eines **Assemblyelements beschreibt die assemblyIdentity** die parallele Assembly, für die mindestens **eine Assembly-** Abhängigkeit geändert wurde. Die Verleger Konfigurationsdatei leitet die Abhängigkeiten der identifizierten Assembly um. Beispielsweise gibt die folgende **assemblyIdentity** an, dass sich die Verleger Konfigurationsdatei auf die Abhängigkeiten der x86-Assembly Microsoft. Windows. Pop 6.0.0.0 auswirkt.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity eine parallele Assemblyabhängigkeit** . Die Verleger Konfigurationsdatei konfiguriert die Identität dieser erforderlichen parallelen Assembly neu. Die Änderung wird in einem **bindingRedirect**-Wert angegeben. Beispielsweise wird durch die folgende **assemblyIdentity** jede Abhängigkeit von Microsoft. Windows. SampleAssembly Version 2.0.0.0 in eine Abhängigkeit von Microsoft. Windows. SampleAssembly Version 2.0.1.0 geändert.

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

Das **assemblyIdentity** -Element verfügt über die folgenden Attribute. Sie verfügt über keine untergeordneten Elemente.



| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Gibt den Assemblytyp an. Erforderlich. In der **assemblyIdentity** für die betroffene Assembly muss der Wert des **Type** -Attributs auf Win32-Policy festgelegt werden. Der Wert Win32-Policy muss in Kleinbuchstaben angegeben werden.<br/> In der **assemblyIdentity für die veränderliche Assemblyabhängigkeit** muss der Wert des **Type** -Attributs auf Win32 festgelegt werden. Der Wert Win32 muss in Kleinbuchstaben angegeben werden.<br/>                                                                                                                                                                                                             |
| **name**                  | Benennt eine Assembly eindeutig. Erforderlich. In der **assemblyIdentity** für die betroffene Assembly weist Name die Formular *Richtlinie* auf. *Haupt* Version. *neben* Version. *AssemblyName* , wobei " *Major* " und " *Minor* " auf die Haupt-und neben Teile der Assemblyversion verweisen. [](assembly-versions.md)<br/> In der **assemblyIdentity für die veränderliche Assemblyabhängigkeit** hat der Name das Format Organization.Division.Name. Beispiel: Microsoft. Windows. MySampleApp.<br/>                                                                                                                                                                                 |
| **language**              | Gibt die Sprache der Assembly an. Dies ist optional. Geben Sie in der **assemblyIdentity** für die betroffene Assembly den DHTML-Sprachcode an, wenn die Assembly sprachspezifisch ist. Wenn die Assembly für die weltweite Verwendung (Sprachneutral) verwendet wird, lassen Sie dieses Attribut aus.<br/> Geben Sie in der **assemblyIdentity für die Änderung der Assemblyabhängigkeit** , wenn die Assembly sprachspezifisch ist, den Code der DHTML-Sprache an. Wenn die Assembly für den weltweiten Gebrauch (Sprachneutral) verwendet wird, legen Sie den Wert auf " \* " fest.<br/>                                                                                                                            |
| **processorArchitecture** | Gibt den Prozessor an, auf dem die Anwendung ausgeführt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Gibt die Assemblyversion an. Verwenden Sie die vierteilige Versions Syntax: mmmm. nnnn. oooo. pppp Nur in der "Def-Context"- **Assemblyidentität** erforderlich. Geben Sie das Versions Attribut nicht in der Ref-Context- **Assemblyidentität** an.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **PublicKeyToken**        | Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein. Ein PublicKeyToken ist für alle freigegebenen parallelen Assemblys erforderlich. Das für die Verleger Konfigurationsdatei verwendete PublicKeyToken muss der gleiche Schlüssel sein, der für die signierte Assembly verwendet wird. Die Verleger Konfigurationsdateien können mit denselben Tools signiert werden, [die auch mit](assembly-signing-example.md) Assemblys verwendet werden [](creating-signed-files-and-catalogs.md) |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**gkeit**
</dt> <dd>

Ein optionales Containerelement für mindestens eine **dependentAssembly**. Sie besitzt keine Attribute.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Jede **dependentAssembly** muss sich in genau einer **Abhängigkeit** befinden. Eine **dependentAssembly** weist keine Attribute auf. Das erste untergeordnete Element von **dependentAssembly** muss eine **assemblyIdentity** sein, damit die parallele Assembly von der Verleger Konfiguration neu konfiguriert wird.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

Das **bindingRedirect** -Element enthält Umleitungs Informationen für die Bindung der Assembly.

Dieses Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.



| Attribut      | BESCHREIBUNG                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OldVersion** | Gibt die Assemblyversion an, die überschrieben und umgeleitet wird. Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn. Geben Sie einen Bereich von Versionen durch einen Bindestrich ohne Leerzeichen an. Beispielsweise 2.14.3.0 oder 2.14.3.0 2.16.0.0. Erforderlich. |
| **NewVersion** | Gibt die Version der Ersetzungs-Assembly an. Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In den Verleger Konfigurationsdateien werden keine Dateien angegeben. Beachten Sie, dass sprachspezifische Richtlinien Dateien von der Verleger Konfigurationsdatei getrennt sind.

## <a name="example"></a>Beispiel

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




