---
description: Wenn Sie möchten, dass Benutzer Ihrer Anwendung bzw. Kern-dll die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satelliten Ressourcen-DLLs zu platzieren.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Verwenden von Assemblys mit einer mehrsprachigen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750945"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Verwenden von Assemblys mit einer mehrsprachigen Benutzeroberfläche

Wenn Sie möchten, dass Benutzer Ihrer Anwendung bzw. Kern-dll die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satelliten Ressourcen-DLLs zu platzieren. Weitere Informationen zum Verwenden von Satelliten Ressourcen-DLLs finden Sie unter [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).

Jede Satelliten-DLL enthält die Ressourcen für eine andere Sprache. Die Core-dll kann als Assembly bereitgestellt werden, und jede der Satelliten-DLLs kann als separate Satellitenassemblys bereitgestellt werden. In diesem Fall sollte jede Satellitenassembly über ein eigenes selbst beschreibendes Assemblymanifest verfügen. Das Manifest der Satellitenassembly sollte keine Abhängigkeit von anderen Assemblys beschreiben. Eine beliebige Abhängigkeit von Satellitenassemblys für andere Assemblys sollte stattdessen im Manifest der Kernassembly beschrieben werden.

Mithilfe der [MUI-Version (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) von Windows können Benutzer die Benutzeroberflächen Sprache gemäß Ihren Einstellungen angeben, vorausgesetzt, die erforderliche Sprache wurde dem System hinzugefügt. Eine Kernassembly kann mehrere Sprachen unterstützen, indem mehrere MUI-Assemblys verwendet werden. In diesem Fall sollte jede MUI-Assembly über ein eigenes Manifest verfügen, und alle Abhängigkeiten von anderen Assemblys sollten nur im Manifest der Kernassembly beschrieben werden.

Proseware. Sample. Pop kann z. b. eine zentrale parallele Assembly sein, die von der Proseware. Research. SampleAssembly-Assembly abhängig ist. Wenn "Proseware. Sample. Pop" MUI verwendet, um mehrere Sprachen zu unterstützen, können separate MUI-Assemblys für jede Sprache bereitgestellt werden. Jede MUI-Assembly sollte über ein eigenes Manifest verfügen, das diese spezielle Satelliten Ressourcen-DLL beschreibt. Die MUI-Assemblymanifeste sollten keinen Verweis auf Abhängigkeiten von anderen Assemblys enthalten. Das Manifest, in dem die Kernassembly "Proseware. Sample. Pop" beschrieben wird, sollte die Abhängigkeit von "Proseware. Sample. Pop" in der Assembly "Proseware. Research. SampleAssembly" beschreiben.

Die Attribute des **assemblyIdentity** -Elements einer Satellitenassembly ähneln denen im Manifest der basisassembly. Das **Name** -Attribut muss mit dem Hinzufügen von "Resources" identisch mit der basisassembly sein. Wenn der Name z. b. "Proseware. Tools. Rechtschreib Check. Runtime-Libraries" in der basisassembly lautet, lautet der Name in der Ressourcenassembly "Proseware. Tools. Rechtschreib Check. Runtime-Libraries. Resources". Mit dem **Language** -Attribut sollte die Sprache der Ressourcenassembly identifiziert werden. Das **File** -Attribut sollte die Liste der Dateien enthalten, bei denen es sich um Ressourcen-DLLs handelt.

Im folgenden finden Sie ein Beispiel für das Manifest für die Ressourcenassembly Proseware. Tools. SpellCheck. Runtime-Libraries.

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

Die basisassembly beschreibt eine optionale Abhängigkeit von der Ressourcenassembly. Wenn ein Benutzer in diesem Beispiel Windows mit dem als Deutsch bezeichneten Gebiets Schema ausgeführt wird, würde eine Anwendung, die die Proseware. Tools. SpellCheck-Assembly verwendet, Text in Deutsch anzeigen.

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

 

 
