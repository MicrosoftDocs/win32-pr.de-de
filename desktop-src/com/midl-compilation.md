---
title: Kompilierung in mittlerer l
description: Kompilierung in mittlerer l
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474341"
---
# <a name="midl-compilation"></a>Kompilierung in mittlerer l

Wenn eine IDL-Datei, wie z [. b. "example2". idl](anatomy-of-an-idl-file.md), eine oder mehrere COM-Schnittstellen und eine Typbibliothek definiert, generiert der mittlerer l-Compiler (Midl.exe) die in der folgenden Tabelle beschriebenen Dateien als Standardausgabe.



| Dateiname                 | BESCHREIBUNG                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Example2". h<br/>    | Die Header Datei, die Typdefinitionen und Funktions Deklarationen für alle Schnittstellen enthält, die in der IDL-Datei definiert sind, sowie vorwärts Deklarationen für Routinen, die vom stubbefehl aufgerufen werden.<br/> |
| "Example2" \_ p. c<br/> | Die Proxy-/Stubdatei, die die Ersatz Einstiegspunkte für-Clients und für-Server enthält.<br/>                                                                                           |
| "Example2" \_ i. c<br/> | Die Schnittstellen-ID-Datei, die die GUID für jede Schnittstelle definiert, die in der IDL-Datei angegeben ist.<br/>                                                                                               |
| "Example2". tlb<br/>  | Eine Verbund Dokument Datei, die Informationen zu Typen und Objekten enthält.<br/>                                                                                                                |
| Dlldata. c<br/>     | Enthält die Daten, die Sie benötigen, um eine Proxy-/Stub-DLL zu erstellen.<br/>                                                                                                                                     |



 

Verwenden Sie die Header Datei und alle c-Dateien, um [eine Proxy-dll zu erstellen](building-and-registering-a-proxy-dll.md) , die die-Schnittstelle unterstützen kann, wenn Sie sowohl von Client Anwendungen als auch von Objekt Servern verwendet wird. \_Beim Erstellen der ausführbaren Datei für eine Client Anwendung, die die-Schnittstelle verwendet, verwenden Sie die Schnittstellen Header Datei ("example2". h) und die Interface-ID-Datei ("example2" i. c). Sie können wählen, ob Sie die Typbibliotheks Datei als Ressource in die exe-oder DLL-Datei einschließen möchten, oder Sie können Sie als separate Datei versenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Für eine COM-Schnittstelle generierte Dateien](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Mittel l-Compileroptionen](midl-compiler-options.md)
</dt> </dl>

 

