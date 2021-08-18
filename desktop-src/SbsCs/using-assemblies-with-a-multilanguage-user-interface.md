---
description: Wenn Sie möchten, dass Benutzer Ihrer Anwendung oder Kern-DLL die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satellitenressourcen-DLLs zu platzieren.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Verwenden von Assemblys mit einem mehrsprachigen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4cd857cca0188b10f02ba44b5631895a9345ce7926cae78376edd554035ccfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141773"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Verwenden von Assemblys mit einem mehrsprachigen Benutzeroberfläche

Wenn Sie möchten, dass Benutzer Ihrer Anwendung oder Kern-DLL die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satellitenressourcen-DLLs zu platzieren. Weitere Informationen zur Verwendung von Satellitenressourcen-DLLs finden Sie unter [Multilanguage Benutzeroberfläche (CSV).](/windows/desktop/Intl/multilingual-user-interface)

Jede Satelliten-DLL enthält die Ressourcen für eine andere Sprache. Die Kern-DLL kann als Assembly bereitgestellt werden, und jede der Satelliten-DLLs kann als separate Satellitenassemblys bereitgestellt werden. In diesem Fall sollte jede Satellitenassembly über ein eigenes selbstbeschreibendes Assemblymanifest verfügen. Das Manifest der Satellitenassembly sollte keine Abhängigkeit von anderen Assemblys beschreiben. Jede Abhängigkeit von Satellitenassemblys von anderen Assemblys sollte stattdessen im Manifest der Kernassembly beschrieben werden.

Mit der [Version von multilanguage Benutzeroberfläche (USERNAME)](/windows/desktop/Intl/multilingual-user-interface) von Windows können Benutzer die Sprache der Benutzeroberfläche gemäß ihren Einstellungen angeben, vorausgesetzt, die erforderliche Sprache wurde dem System hinzugefügt. Eine Kernassembly kann mehrere Sprachen unterstützen, indem mehrere ASSEMBLE-Assemblys verwendet werden. In diesem Fall sollte jede CAB-Assembly über ein eigenes Manifest verfügen, und alle Abhängigkeiten von anderen Assemblys sollten nur im Manifest der Kernassembly beschrieben werden.

Proseware.Sample.Pop kann beispielsweise eine kernseitige Assembly sein, die von der Proseware.Research.SampleAssembly-Assembly abhängig ist. Wenn Proseware.Sample.Pop ZUR Unterstützung mehrerer Sprachen MITHILFE von SEPARATOR arbeitet, können für jede Sprache separate CAB-Assemblys bereitgestellt werden. Jede ASSEMBLE-Assembly sollte über ein eigenes Manifest verfügen, das diese spezielle Satellitenressourcen-DLL beschreibt. Die ASSEMBLE-Assemblymanifeste dürfen keinen Verweis auf Abhängigkeiten von anderen Assemblys enthalten. Das Manifest, das die Kernassembly proseware.Sample.Pop beschreibt, sollte die Abhängigkeit von Proseware.Sample.Pop von der Proseware.Research.SampleAssembly-Assembly beschreiben.

Die Attribute des **assemblyIdentity-Elements** einer Satellitenassembly ähneln denen im Manifest der Basisassembly. Das **Name-Attribut** sollte mit der Basisassembly mit dem Zusatz "Resources" identisch sein. Wenn der Name in der Basisassembly beispielsweise "Proseware.Tools.SpellCheck.Runtime-Libraries" lautet, lautet der Name in der Ressourcenassembly "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources". Das  Sprachattribut sollte die Sprache der Ressourcenassembly identifizieren. Das  Dateiattribut sollte die Liste der Dateien enthalten, bei denen es sich um Ressourcen-DLLs handelt.

Im Folgenden finden Sie ein Beispiel für das Manifest für die Ressourcenassembly Proseware.Tools.SpellCheck.Runtime-Libraries.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

Die Basisassembly beschreibt eine optionale Abhängigkeit von der Ressourcenassembly. Wenn in diesem Beispiel ein Benutzer Windows mit dem gebietsschema ausführt, das als Deutsch festgelegt ist, zeigt eine Anwendung, die die Proseware.Tools.SpellCheck-Assembly verwendet, Text auf Deutsch an.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
